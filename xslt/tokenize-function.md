# fn:tokenize

## Description

The fn:tokenize function splits a string based on a regular expression.

## Arguments and Return Type

| Name     | Type      | Description                                                 |
|----------|-----------|-------------------------------------------------------------|
| $input   | xs:string | the string to tokenize                                      |
| $pattern | xs:string | regular expression to match the delimiters                  |
| $flags   | xs:string | flags that control multiline mode, case insensitivity, etc. |

## Example

How to use tokenize inside a for-each function select attribute

```xsl
<xsl:for-each select="tokenize('a,b,c', ',')">
    // code to be executed
</xsl:for-each>
```

[xsltfunctions.com](http://www.xsltfunctions.com/xsl/fn_tokenize.html)