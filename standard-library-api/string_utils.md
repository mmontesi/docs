# StringUtils

Inclusion code: 

| Service Deployment |  |  |  |
| :--- | :--- | :--- | :--- |
| Port Name | Location | Protocol | Interfaces |
| StringUtils documentation: |  |  |  |
| StringUtils | - | - | [StringUtilsInterface](string_utils.md#StringUtilsInterface) |

### List of Available Interfaces

### StringUtilsInterface <a id="StringUtilsInterface"></a>

Interface documentation: An interface for supporting string manipulation operations.

| Operation Name | Input Type | Output Type | Faults |
| :--- | :--- | :--- | :--- |
| [leftPad](string_utils.md#leftPad) | [PadRequest](string_utils.md#PadRequest) | string |  |
| [valueToPrettyString](string_utils.md#valueToPrettyString) | undefined | string |  |
| [toLowerCase](string_utils.md#toLowerCase) | string | string |  |
| [length](string_utils.md#length) | string | int |  |
| [match](string_utils.md#match) | [MatchRequest](string_utils.md#MatchRequest) | [MatchResult](string_utils.md#MatchResult) |  |
| [replaceFirst](string_utils.md#replaceFirst) | [ReplaceRequest](string_utils.md#ReplaceRequest) | string |  |
| [sort](string_utils.md#sort) | [StringItemList](string_utils.md#StringItemList) | [StringItemList](string_utils.md#StringItemList) |  |
| [replaceAll](string_utils.md#replaceAll) | [ReplaceRequest](string_utils.md#ReplaceRequest) | string |  |
| [substring](string_utils.md#substring) | [SubStringRequest](string_utils.md#SubStringRequest) | string |  |
| [getRandomUUID](string_utils.md#getRandomUUID) | void | string |  |
| [rightPad](string_utils.md#rightPad) | [PadRequest](string_utils.md#PadRequest) | string |  |
| [contains](string_utils.md#contains) | [ContainsRequest](string_utils.md#ContainsRequest) | bool |  |
| [split](string_utils.md#split) | [SplitRequest](string_utils.md#SplitRequest) | [SplitResult](string_utils.md#SplitResult) |  |
| [splitByLength](string_utils.md#splitByLength) | [SplitByLengthRequest](string_utils.md#SplitByLengthRequest) | [SplitResult](string_utils.md#SplitResult) |  |
| [trim](string_utils.md#trim) | string | string |  |
| [find](string_utils.md#find) | [MatchRequest](string_utils.md#MatchRequest) | [MatchResult](string_utils.md#MatchResult) |  |
| [endsWith](string_utils.md#endsWith) | [EndsWithRequest](string_utils.md#EndsWithRequest) | bool |  |
| [toUpperCase](string_utils.md#toUpperCase) | string | string |  |
| [join](string_utils.md#join) | [JoinRequest](string_utils.md#JoinRequest) | string |  |
| [indexOf](string_utils.md#indexOf) | [IndexOfRequest](string_utils.md#IndexOfRequest) | IndexOfResponse |  |
| [startsWith](string_utils.md#startsWith) | [StartsWithRequest](string_utils.md#StartsWithRequest) | bool |  |

## Operation Description

### leftPad <a id="leftPad"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
leftPad@StringUtils( request )( response )
```

#### Request type <a id="PadRequest"></a>

Type: PadRequest

```text
type PadRequest: string {
    .length: int
    .char: string
}
```

`PadRequest : string`

* `length : int`
* `char : string`

#### Response type

Type: string

`string : string`

### valueToPrettyString <a id="valueToPrettyString"></a>

Operation documentation: checks if the passed string starts with a given prefix

Invocation template:

```text
valueToPrettyString@StringUtils( request )( response )
```

#### Request type

Type: undefined

`undefined : any`

#### Response type

Type: string

`string : string`

### toLowerCase <a id="toLowerCase"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
toLowerCase@StringUtils( request )( response )
```

#### Request type

Type: string

`string : string`

#### Response type

Type: string

`string : string`

### length <a id="length"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
length@StringUtils( request )( response )
```

#### Request type

Type: string

`string : string`

#### Response type

Type: int

`int : int`

### match <a id="match"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
match@StringUtils( request )( response )
```

#### Request type <a id="MatchRequest"></a>

Type: MatchRequest

```text
type MatchRequest: string {
    .regex: string
}
```

`MatchRequest : string`

* `regex : string`

#### Response type <a id="MatchResult"></a>

Type: MatchResult

```text
type MatchResult: int {
    .group*: string
}
```

`MatchResult : int`

* `group : string`

### replaceFirst <a id="replaceFirst"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
replaceFirst@StringUtils( request )( response )
```

#### Request type <a id="ReplaceRequest"></a>

Type: ReplaceRequest

```text
type ReplaceRequest: string {
    .regex: string
    .replacement: string
}
```

`ReplaceRequest : string`

* `regex : string`
* `replacement : string`

#### Response type

Type: string

`string : string`

### sort <a id="sort"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
sort@StringUtils( request )( response )
```

#### Request type <a id="StringItemList"></a>

Type: StringItemList

```text
type StringItemList: void {
    .item*: string
}
```

`StringItemList : void`

* `item : string`

#### Response type <a id="StringItemList"></a>

Type: StringItemList

```text
type StringItemList: void {
    .item*: string
}
```

`StringItemList : void`

* `item : string`

### replaceAll <a id="replaceAll"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
replaceAll@StringUtils( request )( response )
```

#### Request type <a id="ReplaceRequest"></a>

Type: ReplaceRequest

```text
type ReplaceRequest: string {
    .regex: string
    .replacement: string
}
```

`ReplaceRequest : string`

* `regex : string`
* `replacement : string`

#### Response type

Type: string

`string : string`

### substring <a id="substring"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
substring@StringUtils( request )( response )
```

#### Request type <a id="SubStringRequest"></a>

Type: SubStringRequest

```text
type SubStringRequest: string {
    .end: int
    .begin: int
}
```

`SubStringRequest : string`

* `end : int`
* `begin : int`

#### Response type

Type: string

`string : string`

### getRandomUUID <a id="getRandomUUID"></a>

Operation documentation: it returns a random UUID

Invocation template:

```text
getRandomUUID@StringUtils( request )( response )
```

#### Request type

Type: void

`void : void`

#### Response type

Type: string

`string : string`

### rightPad <a id="rightPad"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
rightPad@StringUtils( request )( response )
```

#### Request type <a id="PadRequest"></a>

Type: PadRequest

```text
type PadRequest: string {
    .length: int
    .char: string
}
```

`PadRequest : string`

* `length : int`
* `char : string`

#### Response type

Type: string

`string : string`

### contains <a id="contains"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
contains@StringUtils( request )( response )
```

#### Request type <a id="ContainsRequest"></a>

Type: ContainsRequest

```text
type ContainsRequest: string {
    .substring: string
}
```

`ContainsRequest : string`

* `substring : string`

#### Response type

Type: bool

`bool : bool`

### split <a id="split"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
split@StringUtils( request )( response )
```

#### Request type <a id="SplitRequest"></a>

Type: SplitRequest

```text
type SplitRequest: string {
    .regex: string
    .limit?: int
}
```

`SplitRequest : string`

* `regex : string`
* `limit : int`

#### Response type <a id="SplitResult"></a>

Type: SplitResult

```text
type SplitResult: void {
    .result*: string
}
```

`SplitResult : void`

* `result : string`

### splitByLength <a id="splitByLength"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
splitByLength@StringUtils( request )( response )
```

#### Request type <a id="SplitByLengthRequest"></a>

Type: SplitByLengthRequest

```text
type SplitByLengthRequest: string {
    .length: int
}
```

`SplitByLengthRequest : string`

* `length : int`

#### Response type <a id="SplitResult"></a>

Type: SplitResult

```text
type SplitResult: void {
    .result*: string
}
```

`SplitResult : void`

* `result : string`

### trim <a id="trim"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
trim@StringUtils( request )( response )
```

#### Request type

Type: string

`string : string`

#### Response type

Type: string

`string : string`

### find <a id="find"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
find@StringUtils( request )( response )
```

#### Request type <a id="MatchRequest"></a>

Type: MatchRequest

```text
type MatchRequest: string {
    .regex: string
}
```

`MatchRequest : string`

* `regex : string`

#### Response type <a id="MatchResult"></a>

Type: MatchResult

```text
type MatchResult: int {
    .group*: string
}
```

`MatchResult : int`

* `group : string`

### endsWith <a id="endsWith"></a>

Operation documentation: checks if a string ends with a given suffix

Invocation template:

```text
endsWith@StringUtils( request )( response )
```

#### Request type <a id="EndsWithRequest"></a>

Type: EndsWithRequest

```text
type EndsWithRequest: string {
    .suffix: string
}
```

`EndsWithRequest : string`

* `suffix : string`

#### Response type

Type: bool

`bool : bool`

### toUpperCase <a id="toUpperCase"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
toUpperCase@StringUtils( request )( response )
```

#### Request type

Type: string

`string : string`

#### Response type

Type: string

`string : string`

### join <a id="join"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
join@StringUtils( request )( response )
```

#### Request type <a id="JoinRequest"></a>

Type: JoinRequest

```text
type JoinRequest: void {
    .piece*: string
    .delimiter: string
}
```

`JoinRequest : void`

* `piece : string`
* `delimiter : string`

#### Response type

Type: string

`string : string`

### indexOf <a id="indexOf"></a>

Operation documentation: Returns true if the string contains .substring

Invocation template:

```text
indexOf@StringUtils( request )( response )
```

#### Request type <a id="IndexOfRequest"></a>

Type: IndexOfRequest

```text
type IndexOfRequest: string {
    .word: string
}
```

`IndexOfRequest : string`

* `word : string`

#### Response type

Type: IndexOfResponse

`IndexOfResponse : int`

### startsWith <a id="startsWith"></a>

Operation documentation: checks if the passed string starts with a given prefix

Invocation template:

```text
startsWith@StringUtils( request )( response )
```

#### Request type <a id="StartsWithRequest"></a>

Type: StartsWithRequest

```text
type StartsWithRequest: string {
    .prefix: string
}
```

`StartsWithRequest : string`

* `prefix : string`

#### Response type

Type: bool

`bool : bool`

