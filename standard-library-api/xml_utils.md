# XmlUtils

Inclusion code: 

| Service Deployment |  |  |  |
| :--- | :--- | :--- | :--- |
| Port Name | Location | Protocol | Interfaces |
| XmlUtils documentation: |  |  |  |
| XmlUtils | - | - | [XmlUtilsInterface](xml_utils.md#XmlUtilsInterface) |

### List of Available Interfaces

### XmlUtilsInterface <a id="XmlUtilsInterface"></a>

Interface documentation:

| Operation Name | Input Type | Output Type | Faults |
| :--- | :--- | :--- | :--- |
| [xmlToValue](xml_utils.md#xmlToValue) | [XMLToValueRequest](xml_utils.md#XMLToValueRequest) | undefined |  IOException\( [IOExceptionType](xml_utils.md#IOExceptionType) \) |
| [transform](xml_utils.md#transform) | [XMLTransformationRequest](xml_utils.md#XMLTransformationRequest) | string |  TransformerException\( [JavaExceptionType](xml_utils.md#JavaExceptionType) \) |
| [valueToXml](xml_utils.md#valueToXml) | [ValueToXmlRequest](xml_utils.md#ValueToXmlRequest) | string |  IOException\( [IOExceptionType](xml_utils.md#IOExceptionType) \)  IllegalArgumentException\( string \) |

## Operation Description

### xmlToValue <a id="xmlToValue"></a>

Operation documentation: Transforms the base value in XML format \(data types string, raw\) into a Jolie value

```text
      The XML root node will be discarded, the rest gets converted recursively
```

Invocation template:

```text
xmlToValue@XmlUtils( request )( response )
```

#### Request type <a id="XMLToValueRequest"></a>

Type: XMLToValueRequest

```text
type XMLToValueRequest: any {
    .options?: void {
        .skipMixedText?: bool
        .charset?: string
        .includeAttributes?: bool
        .schemaLanguage?: string
        .includeRoot?: bool
        .schemaUrl?: string
    }
    .isXmlStore?: bool
}
```

`XMLToValueRequest : any`

* `options : void`
  * `skipMixedText : bool`
  * `charset : string`
  * `includeAttributes : bool`
  * `schemaLanguage : string`
  * `includeRoot : bool`
  * `schemaUrl : string`
* `isXmlStore : bool`

#### Response type

Type: undefined

`undefined : any`

#### Possible faults thrown

Fault `IOException` with type `IOExceptionType`

Fault-handling install template:

```text
install ( IOException => /* error-handling code */ )
```

```text
type IOExceptionType: JavaExceptionType
```

### transform <a id="transform"></a>

Operation documentation:

Invocation template:

```text
transform@XmlUtils( request )( response )
```

#### Request type <a id="XMLTransformationRequest"></a>

Type: XMLTransformationRequest

```text
type XMLTransformationRequest: void {
    .source: string
    .xslt: string
}
```

`XMLTransformationRequest : void`

* `source : string`
* `xslt : string`

#### Response type

Type: string

`string : string`

#### Possible faults thrown

Fault `TransformerException` with type `JavaExceptionType`

Fault-handling install template:

```text
install ( TransformerException => /* error-handling code */ )
```

```text
type JavaExceptionType: string {
    .stackTrace: string
}
```

### valueToXml <a id="valueToXml"></a>

Operation documentation: Transforms the value contained within the root node into an xml string.

```text
      The base value of ValueToXmlRequest.root will be discarded, the rest gets converted recursively
```

Invocation template:

```text
valueToXml@XmlUtils( request )( response )
```

#### Request type <a id="ValueToXmlRequest"></a>

Type: ValueToXmlRequest

```text
type ValueToXmlRequest: void {
    .omitXmlDeclaration?: bool
    .indent?: bool
    .plain?: bool
    .root: undefined
    .rootNodeName?: string
    .isXmlStore?: bool
    .applySchema?: void {
        .schema: string
        .doctypeSystem?: string
        .encoding?: string
    }
}
```

`ValueToXmlRequest : void`

* `omitXmlDeclaration : bool`
* `indent : bool`
* `plain : bool`
* `root : any`
* `rootNodeName : string`
* `isXmlStore : bool`
* `applySchema : void`
  * `schema : string`
  * `doctypeSystem : string`
  * `encoding : string`

#### Response type

Type: string

`string : string`

#### Possible faults thrown

Fault `IOException` with type `IOExceptionType`

Fault-handling install template:

```text
install ( IOException => /* error-handling code */ )
```

```text
type IOExceptionType: JavaExceptionType
```

Fault `IllegalArgumentException` with type `string`

Fault-handling install template:

```text
install ( IllegalArgumentException => /* error-handling code */ )
```

### Subtypes

#### JavaExceptionType <a id="JavaExceptionType"></a>

```
type JavaExceptionType: string { .stackTrace: string }
```

