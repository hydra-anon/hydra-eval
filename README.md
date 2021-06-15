# Hydra evaluation results

This page presents the detailed results of the evaluation of the XSS prototype of Hydra, a feedback-driven approach for the dynamic exploitation of injection vulnerabilities.

## Errata

The following issues are present in the most recent submitted version of our work. They will be corrected as soon as possible.

* The tools legend in the figures detailing the results of the evaluation do not explain what "Hydra", "HydraShort" and "HydraStatic" mean. "HydraShort" is Hydra using the XSS polyglot shortcut. "Hydra" is the dynamic version of Hydra without using the polyglot. "HydraStatic" is the static version of Hydra without using the polyglot.


## Overview

The following table briefly summarizes the success rate of the investigated tools when applied to various SUTs. Please note that SUTs that could not be exploited by any of the tools are excluded here.

Application | HydraShort+Hydra | HydraShort | Hydra | HydraStatic | w3af | AppScan
-------- | -------- | -------- | -------- | -------- | -------- | -------
WAVSEP      | 39/41 | 9/41  | 37/41 | 35/41 | 38/41 | 23/41
FiringRange | 56/73 | 34/73 | 54/73 | 48/73 | 61/73 | 27/73
Juice Shop  | 1/1   | 1/1   | 0/1   | 1/1   | 0/1   | 0/1
MyBB        | 1/1   | 1/1   | 0/1   | 0/1   | 0/1   | 1/1
MaraCMS     | 1/1   | 1/1   | 1/1   | 1/1   | 1/1   | 1/1
Tailor      | 1/1   | 1/1   | 1/1   | 1/1   | 0/1   | 1/1
TestLink    | 2/2   | 2/2   | 2/2   | 2/2   | 0/2   | 0/2


## WAVSEP

ID  | Title | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------ | ------
B01 | Case 1 - RXSS via tag injection into the scope of an HTML page | ✓ | ✓ | ✓ | ✓ | ✓
B02 | Case 2 - RXSS via tag injection into the scope of an HTML tag | ✓ | ✕ | ✕ | ✓ | ✕
B03 | Case 3 - RXSS via tag injection into the scope of an HTML tag structure | ✓ | ✓ | ✕ | ✓ | ✓
B04 | Case 4 - RXSS via tag injection into the scope of an HTML comment | ✓ | ✓ | ✓ | ✓ | ✓
B05 | Case 5 - RXSS via frame tag injection into the scope of an HTML frameset | ✕ | ✓ | ✓ | ✓ | ✓
B06 | Case 6 - RXSS via DHTML event injection into the scope of an HTML tag | ✕ | ✓ | ✓ | ✓ | ✓
B07 | Case 7 - RXSS via DHTML event injection into the scope of an HTML property (Double Quote Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B08 | Case 8 - RXSS via DHTML event injection into the scope of an HTML property (Single Quote Delimiter) | ✕ | ✓ | ✓ | ✓ | ✕
B09 | Case 9 - RXSS via src property injection into the scope of an HTML tag structure (RFI) | ✕ | ✓ | ✕ | ✓ | ✓
B10 | Case 10 - RXSS via Javascript injection into the scope of an HTML/Javascript Event (Double Quote Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B11 | Case 11 - RXSS via Javascript injection into the scope of an HTML/Javascript Event (Single Quote Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B12 | Case 12 - RXSS via Javascript injection into the scope of an HTML/Javascript Event (Any Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B13 | Case 13 - RXSS via VBScript injection into the scope of an HTML/VBScript Event (Double Quote Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B14 | Case 14 - RXSS via VBScript injection into the scope of an HTML/VBScript Event (Single Quote Delimiter) | ✕ | ✓ | ✓ | ✓ | ✕
B15 | Case 15 - RXSS via VBScript injection into the scope of an HTML/VBScript Event (Any Delimiter) | ✕ | ✓ | ✓ | ✓ | ✕
B16 | Case 16 - RXSS via Javascript injection into the scope of a script supporting property | ✓ | ✓ | ✓ | ✓ | ✓
B17 | Case 17 - RXSS via Javascript injection into the scope of javascript code within a property (Double Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B18 | Case 18 - RXSS via Javascript injection into the scope of javascript code within a property (Single Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B19 | Case 19 - RXSS via Javascript injection into the scope of javascript code within a property (No String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B20 | Case 20 - RXSS via VBScript injection into the scope of VBScript code within a property (Double Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B21 | Case 21 - RXSS via VBScript injection into the scope of VBScript code within a property (Single Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✕
B22 | Case 22 - RXSS via Javascript injection into the scope of a script tag (Javascript, Double Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B23 | Case 23 - RXSS via Javascript injection into the scope of a script tag (Javascript, Single Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B24 | Case 24 - RXSS via Javascript injection into the scope of a script tag (Javascript, No String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✓
B25 | Case 25 - RXSS via VBScript injection into the scope of a script tag (VBScript, Double Quote String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✕
B26 | Case 26 - RXSS via VBScript injection into the scope of a script tag (VBScript, No String Delimiter) | ✕ | ✓ | ✓ | ✓ | ✕
B27 | Case 27 - RXSS via Javascript injection into the scope of a script tag single line comment | ✕ | ✓ | ✓ | ✓ | ✕
B28 | Case 28 - RXSS via Javascript injection into the scope of a script tag multiline comment | ✓ | ✓ | ✓ | ✓ | ✕
B29 | Case 29 - RXSS via VBScript injection into the scope of a script tag single line comment | ✕ | ✓ | ✓ | ✓ | ✕
B30 | Case 30 - RXSS via tag injection into the scope of an HTML page (Multiple RXSS Vulnerabilities) | ✓ | ✓ | ✓ | ✓ | ✓
B31 | Case 31 - RXSS via tag injection into the scope of an HTML page (during an exception) | ✕ | ✕ | ✕ | ✓ | ✕
B32 | Case 32 - RXSS via tag injection into the scope of an HTML page (Viewstate Required) | ✓ | ✕ | ✕ | ✓ | ✓
E01 | Case 1 - RXSS via tag injection into the scope of an HTML page that Strips Script Tags | ✓ | ✓ | ✓ | ✓ | ✓
E02 | Case 2 - RXSS via tag injection into the scope of an HTML page that only relies on secret POST input | ✕ | ✕ | ✕ | ✕ | ✕
E03 | Case 3 - RXSS via tag injection into the scope of an HTML page that requires a constant session stored AntiCSRF token | ✕ | ✕ | ✕ | ✓ | ✓
E04 | Case 4 - RXSS via tag injection into the scope of an HTML page that requires an expiring one-use session stored AntiCSRF token | ✕ | ✕ | ✕ | ✕ | ✕
E05 | Scriptless Injection in HTML Form Tag Action Attribute scope of the HTML page. | ✕ | ✓ | ✓ | ✕ | ✕
E06 | Scriptless Injection in HTML Base Tag Href Attribute scope of the HTML page. | ✕ | ✓ | ✓ | ✕ | ✕
E07 | Scriptless Injection in HTML Script Tag Src Attribute scope of the HTML page. | ✕ | ✓ | ✓ | ✕ | ✕
E08 | RXSS Injection in CSS Selector | ✕ | ✓ | ✓ | ✓ | ✕
E09 | RXSS Injection in CSS Selector Atrribute Name | ✕ | ✓ | ✓ | ✓ | ✕
E10 | RXSS Injection in CSS Property | ✕ | ✓ | ✓ | ✓ | ✕
E11 | RXSS Injection in CSS Property Value | ✕ | ✓ | ✓ | ✓ | ✕


## Firing Range

ID  | Title | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------ | ------
F1 | Body - HTML escaped | ✕ | ✕ | ✕ | ✕ | ✕
F2 | Body - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F3 | Head - HTML escaped | ✕ | ✕ | ✕ | ✕ | ✕
F4 | Head - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F5 | Body HTML comment - HTML escaped | ✕ | ✕ | ✕ | ✕ | ✕
F6 | Body HTML comment - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F7 | Textarea - HTML escaped | ✕ | ✕ | ✕ | ✕ | ✕
F8 | Textarea - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F9 | Tag name - HTML escaped | ✕ | ✕ | ✕ | ✕ | ✕
F10 | Tag name - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F11 | Attribute unquoted - HTML escaped | ✕ | ✕ | ✕ | ✓ | ✕
F12 | Attribute unquoted - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F13 | Attribute single quoted - HTML escaped | ✕ | ✕ | ✕ | ✓ | ✕
F14 | Attribute single quoted - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F15 | Attribute double quoted - HTML escaped | ✕ | ✕ | ✕ | ✓ | ✕
F16 | Attribute double quoted - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F17 | Attribute name - HTML escaped | ✕ | ✕ | ✕ | ✓ | ✕
F18 | Attribute name - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F19 | CSS - HTML escaped | ✕ | ✓ | ✓ | ✓ | ✕
F20 | CSS - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F21 | CSS Value - HTML escaped | ✕ | ✓ | ✓ | ✓ | ✕
F22 | CSS Value - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F23 | CSS Font Name - HTML escaped | ✕ | ✓ | ✓ | ✓ | ✕
F24 | CSS Font Name - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F25 | Javascript unquoted assignment - HTML escaped | ✕ | ✓ | ✓ | ✓ | ✕
F26 | Javascript unquoted assignment - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F27 | Javascript eval - HTML escaped | ✓ | ✓ | ✓ | ✓ | ✕
F28 | Javascript eval - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F29 | Javascript quoted string - HTML escaped | ✓ | ✓ | ✓ | ✓ | ✕
F30 | Javascript quoted string - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F31 | Javascript single quoted string - HTML escaped | ✓ | ✓ | ✓ | ✓ | ✕
F32 | Javascript single quoted string - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F33 | Javascript slash quoted string - HTML escaped | ✓ | ✓ | ✓ | ✓ | ✕
F34 | Javascript slash quoted string - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F35 | Javascript comment - HTML escaped | ✓ | ✓ | ✓ | ✓ | ✕
F36 | Javascript comment - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F37 | Script SRC double quoted - HTML escaped | ✕ | ✓ | ✓ | ✓ | ✕
F38 | Script SRC double quoted - URL escaped | ✕ | ✓ | ✓ | ✕ | ✕
F39 | URL - HREF - HTML escaped | ✕ | ✕ | ✕ | ✕ | ✕
F40 | URL - HREF - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F41 | URL - CSS - HTML escaped | ✕ | ✕ | ✕ | ✓ | ✕
F42 | URL - CSS - URL escaped | ✕ | ✕ | ✕ | ✕ | ✕
F43 | Eval payload after applying escape() | ✓ | ✓ | ✓ | ✓ | ✓
F44 | Eval payload after applying encodeURIComponent() | ✓ | ✓ | ✓ | ✓ | ✓
F45 | Eval payload after escaping &lt; | ✓ | ✓ | ✓ | ✓ | ✓
F46 | Parameter - Body | ✓ | ✓ | ✓ | ✓ | ✓
F47 | Parameter - Head | ✓ | ✓ | ✓ | ✓ | ✓
F48 | Parameter - Title | ✓ | ✕ | ✕ | ✓ | ✓
F49 | Parameter - Body HTML comment | ✓ | ✓ | ✓ | ✓ | ✓
F50 | Parameter - Tag name | ✓ | ✓ | ✓ | ✓ | ✓
F51 | Parameter - Attribute unquoted | ✓ | ✓ | ✕ | ✓ | ✓
F52 | Parameter - Attribute single quoted | ✓ | ✓ | ✕ | ✓ | ✓
F53 | Parameter - Attribute double quoted | ✓ | ✓ | ✕ | ✓ | ✓
F54 | Parameter - Attribute name | ✓ | ✓ | ✕ | ✓ | ✕
F55 | Parameter - Body - 400 | ✓ | ✓ | ✓ | ✓ | ✕
F56 | Parameter - Body - 401 | ✓ | ✓ | ✓ | ✓ | ✕
F57 | Parameter - Body - 403 | ✓ | ✓ | ✓ | ✓ | ✕
F58 | Parameter - Body - 404 | ✓ | ✓ | ✓ | ✕ | ✕
F59 | Parameter - Body - 500 | ✓ | ✓ | ✓ | ✕ | ✕
F60 | Parameter - iFrame Attribute Value | ✕ | ✕ | ✕ | ✓ | ✓
F61 | Parameter - iFrame srcdoc | ✕ | ✕ | ✕ | ✓ | ✓
F62 | Parameter - Textarea | ✓ | ✕ | ✕ | ✓ | ✕
F63 | Parameter - Textarea Attribute Value | ✕ | ✕ | ✕ | ✓ | ✕
F64 | Parameter - NoScript | ✕ | ✕ | ✕ | ✓ | ✕
F65 | Parameter - Style Attribute Value | ✕ | ✓ | ✕ | ✓ | ✕
F66 | Parameter - CSS | ✓ | ✓ | ✓ | ✓ | ✕
F67 | Parameter - CSS Value | ✓ | ✓ | ✓ | ✓ | ✕
F68 | Parameter - CSS Font Name | ✓ | ✓ | ✓ | ✓ | ✕
F69 | Parameter - unquoted onclick | ✕ | ✕ | ✕ | ✓ | ✓
F70 | Parameter - quoted onclick | ✕ | ✕ | ✕ | ✓ | ✓
F71 | Parameter - quoted onclick | ✕ | ✕ | ✕ | ✓ | ✓
F72 | Parameter - Javascript unquoted assignment | ✓ | ✓ | ✓ | ✓ | ✓
F73 | Parameter - Javascript eval | ✓ | ✓ | ✓ | ✓ | ✓
F74 | Parameter - Javascript quoted string | ✓ | ✓ | ✓ | ✓ | ✓
F75 | Parameter - Javascript single quoted string | ✓ | ✓ | ✓ | ✓ | ✓
F76 | Parameter - Javascript slash quoted string | ✓ | ✓ | ✓ | ✓ | ✓
F77 | Parameter - Javascript comment | ✓ | ✓ | ✓ | ✓ | ✕
F78 | Parameter - Script SRC double quoted | ✕ | ✓ | ✓ | ✓ | ✕
F79 | URL - HREF | ✕ | ✓ | ✓ | ✓ | ✓
F80 | URL - CSS | ✕ | ✕ | ✕ | ✓ | ✓
F81 | URL - Script SRC | ✕ | ✓ | ✓ | ✓ | ✕
F82 | URL - Object DATA | ✕ | ✕ | ✕ | ✕ | ✕
F83 | URL - Param SRC | ✕ | ✕ | ✕ | ✕ | ✕
F84 | Parameter - JSON | ✕ | ✕ | ✕ | ✓ | ✓
F85 | ContentSniffing | ✕ | ✕ | ✕ | ✓ | ✓
F86 | ContentSniffing | ✕ | ✕ | ✕ | ✓ | ✓
F87 | Parameter - Body - Blocks SpaceDoubleQuoteSlashEquals | ✕ | ✓ | ✓ | ✓ | ✕
F88 | Parameter - Attribute unquoted - Blocks DoubleQuoteSinglequote | ✕ | ✓ | ✕ | ✓ | ✕
F89 | Parameter - Body - Blocks lowercase script | ✓ | ✓ | ✓ | ✓ | ✕
F90 | Parameter - Body - Blocks uppercase script | ✓ | ✓ | ✓ | ✓ | ✕
F91 | Parameter - Body - Blocks any script | ✕ | ✓ | ✓ | ✓ | ✕

## Juice Shop

ID  | Title | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------ | ------
Juice | Search request/location hash | ✓ | ✕ | ✓ | ✕ | ✕

## Real-world applications

ID  | Title | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------ | ------
MyBB | MyBB ModCP finduser | ✓ | ✕ | ✕ | ✕ | ✓
Mara | MaraCMS theme | ✓ | ✓ | ✓ | ✓ | ✓
Tailor | Tailor Login | ✓ | ✓ | ✓ | ✕ | ✓
TL01 | TestLink reqURI | ✓ | ✓ | ✓ | ✕ | ✕
TL02 | TestLink show_mode | ✓ | ✓ | ✓ | ✕ | ✕

# Old Appendix

The following material was created based on the original draft of our work.

## WAVSEP

Test case | Polyglot successful? | Best context weight (dynamic) | Best context name (dynamic) | # Requests (dynamic) | Best context weight (static) | Best context name (dynamic) | # Requests (static)
-------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- 
Case01_Tag2HtmlPageScope_jsp_userinput_myinputvalue | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
Case02_Tag2TagScope_jsp_userinput_myinputvalue | yes | 50 | Text node in TEXTAREA | 91 | 50 | Text node in TEXTAREA | 2165
Case03_Tag2TagStructure_jsp_userinput_myinputvalue | yes | 100 | Attribute value in INPUT onclick | 29 | 50 | Attribute value in INPUT value | 1
Case04_Tag2HtmlComment_jsp_userinput_myinputvalue | yes | 100 | Text node in SCRIPT | 31 | 100 | Text node in SCRIPT | 3
Case05_Tag2Frameset_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case06_Event2TagScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in IMG src | 1 | 100 | Attribute value in IMG src | 1
Case07_Event2DoubleQuotePropertyScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in IMG src | 1 | 100 | Attribute value in IMG src | 1
Case08_Event2SingleQuotePropertyScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in IMG src | 1 | 100 | Attribute value in IMG src | 1
Case09_SrcProperty2TagStructure_jsp_userinput_myinputvalue | no | 100 | Attribute value in SCRIPT onload | 163 | 50 | Attribute value in SCRIPT id | 1
Case10_Js2DoubleQuoteJsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
Case11_Js2SingleQuoteJsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
Case12_Js2JsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
Case13_Vbs2DoubleQuoteVbsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
Case14_Vbs2SingleQuoteVbsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
Case15_Vbs2VbsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
Case16_Js2ScriptSupportingProperty_jsp_userinput_myinputvalue_html | yes | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case17_Js2PropertyJsScopeDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case18_Js2PropertyJsScopeSingleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case19_Js2PropertyJsScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case20_Vbs2PropertyVbsScopeDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case21_Vbs2PropertyVbsScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
Case22_Js2ScriptTagDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case23_Js2ScriptTagSingleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case24_Js2ScriptTag_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case25_Vbs2ScriptTagDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case26_Vbs2ScriptTag_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case27_Js2ScriptTagOLCommentScope_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case28_Js2ScriptTagMLCommentScope_jsp_userinput_myinputvalue | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case29_Vbs2ScriptTagOLCommentScope_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Case30_Tag2HtmlPageScopeMultipleVulnerabilities_jsp_userinput_myinputvalue_userinput2_1234 | yes | 100 | Text node in SCRIPT | 6 | 100 | Text node in STYLE | 2
Case32_Tag2HtmlPageScopeValidViewstateRequired_jsp_userinput_myinputvalue_VIEWSTATE | yes |  | 2 | 2 |  |  | 
Experimental_Case01_Tag2HtmlPageScope_StripScriptTag_jsp_userinput_myinputvalue | yes | 100 | Text node in STYLE | 264 | 100 | Text node in STYLE | 2
Experimental_Case02_Tag2HtmlPageScope_SecretVectorPOST_jsp_userinput_myinputvalue | no |  | 1 |  |  |  | 
Experimental_Case03_Tag2HtmlPageScope_ConstantAntiCSRFToken | no |  | 1 |  |  |  | 
Experimental_Case05_ScriptlessInjectionInFormTagActionAttribute_jsp_userinput_myinputvalue | no | 100 | Attribute value in FORM action | 1 | 100 | Attribute value in FORM action | 1
Experimental_Case06_ScriptlessInjectionInBaseTagHrefAttribute_jsp_userinput_myinputvalue | no | 100 | Attribute value in BASE href | 1 | 100 | Attribute value in BASE href | 1
Experimental_Case07_ScriptlessInjectionInScriptTagSrcAttribute_jsp_userinput_myinputvalue | no | 100 | Attribute value in SCRIPT src | 1 | 100 | Attribute value in SCRIPT src | 1
Experimental_Case08_InjectionInToCssSelector_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
Experimental_Case09_InjectionInToCssSelectorAttributeName_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
Experimental_Case10_InjectionInToCssProperty_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
Experimental_Case11_InjectionInToCssPropertyValue_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1

## Firing Range

Test case | Polyglot successful? | Best context weight (dynamic) | Best context name (dynamic) | # Requests (dynamic) | Best context weight (static) | Best context name (dynamic) | # Requests (static)
-------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- 
escape_js_encodeURIComponent_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_js_escape_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_js_html_escape_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_attribute_name_q_teststr | no | 50 | Attribute name in TAG aoeu123%0d%2520%253ehydra%0d+%3ehydra | 157 | 50 | Attribute name in TAG aoeu123 | 1
escape_serverside_encodeUrl_attribute_quoted_q_teststr | no | 50 | Attribute value in TAG attribute | 25 | 50 | Attribute value in TAG attribute | 1
escape_serverside_encodeUrl_attribute_script_q_teststr | no | 100 | Attribute value in SCRIPT src | 1 | 100 | Attribute value in SCRIPT src | 1
escape_serverside_encodeUrl_attribute_singlequoted_q_teststr | no | 50 | Attribute value in TAG attribute | 25 | 50 | Attribute value in TAG attribute | 1
escape_serverside_encodeUrl_attribute_unquoted_q_teststr | no | 50 | Attribute value in TAG attribute | 25 | 50 | Attribute value in TAG attribute | 1
escape_serverside_encodeUrl_body_comment_q_teststr | no | 10 | Comment in BODY | 29 | 10 | Comment in BODY | 2061
escape_serverside_encodeUrl_body_q_teststr | no | 50 | Text node in BODY | 91 | 50 | Text node in BODY | 2048
escape_serverside_encodeUrl_css_import_q_teststr | no | 50 | Attribute value in LINK href | 25 | 50 | Attribute value in LINK href | 1
escape_serverside_encodeUrl_css_style_font_value_q_teststr | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
escape_serverside_encodeUrl_css_style_q_teststr | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
escape_serverside_encodeUrl_css_style_value_q_teststr | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
escape_serverside_encodeUrl_head_q_teststr | no | 50 | Text node in BODY | 91 | 50 | Text node in BODY | 2055
escape_serverside_encodeUrl_js_assignment_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_js_comment_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_js_eval_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_js_quoted_string_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_js_singlequoted_string_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_js_slashquoted_string_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_encodeUrl_tagname_q_teststr | no | 79 | Tag name in AOEU123%0A%3E%3CSTYLE%2FONCLICK | 2045 | 79 | Tag name in AOEU123%3E%3CSCRIPT%259SRC%259%253D%2522HTTPS%3A%2F%2FMATRIS.SBA-RESEARCH.ORG%2FEVIL.JS | 1273
escape_serverside_encodeUrl_textarea_q_teststr | no | 50 | Text node in TEXTAREA | 91 | 50 | Text node in TEXTAREA | 2069
escape_serverside_escapeHtml_attribute_name_q_teststr | no | 50 | Attribute name in TAG &gt;hydra | 157 | 50 | Attribute name in TAG aoeu123 | 1
escape_serverside_escapeHtml_attribute_quoted_q_teststr | no | 50 | Attribute name in TAG &gt;hydra%20%2f%3ehydra\" | 73 | 50 | Attribute value in TAG attribute | 1
escape_serverside_escapeHtml_attribute_script_q_teststr | no | 100 | Attribute value in SCRIPT src | 1 | 100 | Attribute value in SCRIPT src | 1
escape_serverside_escapeHtml_attribute_singlequoted_q_teststr | no | 50 | Attribute name in TAG &gt;hydra%20%2f%3ehydra' | 73 | 50 | Attribute value in TAG attribute | 1
escape_serverside_escapeHtml_attribute_unquoted_q_teststr | no | 50 | Attribute name in TAG %3ehydra%20%2f%3ehydra | 145 | 50 | Attribute value in TAG attribute | 1
escape_serverside_escapeHtml_body_comment_q_teststr | no | 10 | Comment in BODY | 29 | 10 | Comment in BODY | 2061
escape_serverside_escapeHtml_body_q_teststr | no | 50 | Text node in BODY | 91 | 50 | Text node in BODY | 2052
escape_serverside_escapeHtml_css_import_q_teststr | no | 50 | Attribute name in LINK &gt;hydra%20%2f%3ehydra\" | 73 | 50 | Attribute value in LINK href | 1
escape_serverside_escapeHtml_css_style_font_value_q_teststr | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
escape_serverside_escapeHtml_css_style_q_teststr | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
escape_serverside_escapeHtml_css_style_value_q_teststr_escape_HTML_ESCAPE | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
escape_serverside_escapeHtml_head_q_teststr | no | 50 | Text node in BODY | 91 | 50 | Text node in BODY | 2041
escape_serverside_escapeHtml_js_assignment_q_teststr | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_escapeHtml_js_comment_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_escapeHtml_js_eval_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_escapeHtml_js_quoted_string_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_escapeHtml_js_singlequoted_string_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_escapeHtml_js_slashquoted_string_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
escape_serverside_escapeHtml_tagname_q_teststr | no | 50 | Attribute name in AOEU123%2F%3E%3CSVG onclick | 2032 | 50 | Attribute name in AOEU123 evil.js | 1273
escape_serverside_escapeHtml_textarea_q_teststr | no | 50 | Text node in TEXTAREA | 91 | 50 | Text node in TEXTAREA | 2051
reflected_contentsniffing_plaintext_q_teststr | no | 50 | Text node in PRE | 7 | 50 | Text node in PRE | 39
reflected_escapedparameter_js_eventhandler_quoted_DOUBLE_QUOTED_ATTRIBUTE_q_teststr | no | 50 | Attribute value in DIV onclick | 25 | 50 | Attribute value in DIV onclick | 1
reflected_escapedparameter_js_eventhandler_singlequoted_SINGLE_QUOTED_ATTRIBUTE_q_teststr | no | 50 | Attribute value in DIV onclick | 25 | 50 | Attribute value in DIV onclick | 1
reflected_escapedparameter_js_eventhandler_unquoted_UNQUOTED_ATTRIBUTE_q_teststr | no | 50 | Attribute name in DIV %3ehydra%20%2f%3ehydra | 145 | 50 | Attribute value in DIV onclick | 1
reflected_filteredcharsets_attribute_unquoted_DoubleQuoteSinglequote_q_teststr | no | 100 | Text node in SCRIPT | 7 | 50 | Attribute value in TAG attribute | 1
reflected_filteredcharsets_body_SpaceDoubleQuoteSlashEquals_q_teststr | no | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 6
reflected_filteredstrings_body_caseInsensitive_script_q_teststr | no | 100 | Text node in STYLE | 290 | 100 | Text node in STYLE | 2
reflected_filteredstrings_body_caseSensitive_script_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
reflected_filteredstrings_body_caseSensitive_SCRIPT_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
reflected_parameter_attribute_name_q_teststr | yes | 100 | Text node in SCRIPT | 13 | 50 | Attribute name in TAG aoeu123 | 1
reflected_parameter_attribute_quoted_q_teststr | yes | 100 | Text node in SCRIPT | 17 | 50 | Attribute value in TAG attribute | 1
reflected_parameter_attribute_script_q_teststr | no | 100 | Attribute value in SCRIPT src | 1 | 100 | Attribute value in SCRIPT src | 1
reflected_parameter_attribute_singlequoted_q_teststr | yes | 100 | Text node in SCRIPT | 20 | 50 | Attribute value in TAG attribute | 1
reflected_parameter_attribute_unquoted_q_teststr | yes | 100 | Text node in SCRIPT | 7 | 50 | Attribute value in TAG attribute | 1
reflected_parameter_body_400_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
reflected_parameter_body_401_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
reflected_parameter_body_403_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
reflected_parameter_body_404_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
reflected_parameter_body_500_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 3
reflected_parameter_body_comment_q_teststr | yes | 100 | Text node in SCRIPT | 28 | 100 | Text node in SCRIPT | 3
reflected_parameter_body_q_teststr | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 3
reflected_parameter_css_style_font_value_q_teststr | yes | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
reflected_parameter_css_style_q_teststr | yes | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
reflected_parameter_css_style_value_q_teststr | yes | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
reflected_parameter_head_q_teststr | yes | 100 | Text node in SCRIPT | 3 | 100 | Text node in STYLE | 4
reflected_parameter_iframe_attribute_value_q_teststr | no | 50 | Text node in IFRAME | 2044 | 50 | Attribute value in IFRAME attribute | 1
reflected_parameter_iframe_srcdoc_q_teststr | no | 50 | Text node in IFRAME | 2033 | 50 | Attribute value in IFRAME srcdoc | 1
reflected_parameter_js_assignment_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
reflected_parameter_js_comment_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
reflected_parameter_js_eval_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
reflected_parameter_js_quoted_string_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
reflected_parameter_js_singlequoted_string_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
reflected_parameter_js_slashquoted_string_q_teststr | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
reflected_parameter_noscript_q_teststr | no | 50 | Text node in NOSCRIPT | 91 | 50 | Text node in NOSCRIPT | 2065
reflected_parameter_style_attribute_value_q_teststr | no | 100 | Text node in STYLE | 10 | 50 | Attribute value in STYLE attribute | 1
reflected_parameter_tagname_q_teststr | yes | 100 | Text node in SCRIPT | 418 | 100 | Text node in SCRIPT | 2
reflected_parameter_textarea_attribute_value_q_teststr | no | 50 | Text node in TEXTAREA | 2047 | 10 | Attribute value in TEXTAREA attribute | 1
reflected_parameter_textarea_q_teststr | yes | 50 | Text node in TEXTAREA | 91 | 50 | Text node in TEXTAREA | 2080
reflected_parameter_title_q_teststr | yes | 50 | Text node in TITLE | 91 | 50 | Text node in TITLE | 2064
reflected_url_css_import_q_teststr | no | 50 | Attribute value in LINK href | 25 | 50 | Attribute value in LINK href | 1
reflected_url_href_q_teststr | no | 100 | Attribute value in A href | 1 | 100 | Attribute value in A href | 1
reflected_url_object_data_q_teststr | no | 50 | Attribute value in OBJECT data | 59 | 50 | Attribute value in OBJECT data | 1
reflected_url_object_param_q_teststr | no | 50 | Attribute value in PARAM value | 25 | 50 | Attribute value in PARAM value | 1
reflected_url_script_src_q_teststr | no | 100 | Attribute value in SCRIPT src | 1 | 100 | Attribute value in SCRIPT src | 1

## Juice Shop

Test case | Polyglot successful? | Best context weight (dynamic) | Best context name (dynamic) | # Requests (dynamic) | Best context weight (static) | Best context name (dynamic) | # Requests (static)
-------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- 
Juice Shop | yes | 50 | Text node in B | 29 | 100 | Text node in SCRIPT | 1

## Real-Life Vulnerabilities

Test case | Polyglot successful? | Best context weight (dynamic) | Best context name (dynamic) | # Requests (dynamic) | Best context weight (static) | Best context name (dynamic) | # Requests (static)
-------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- 
MaraCMS | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
Tailor | yes | 100 | Text node in SCRIPT | 7 | 100 | Text node in SCRIPT | 2
TestLink (deDeleteStep) | yes | 100 | Text node in SCRIPT | 379 | 100 | Text node in SCRIPT | 2
TestLink (reqURI) | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
MyBB | yes | - | (see paper) | - | - | (see paper) | -

# Additional Material

While we would like to offer a download of the Hydra source code at this time, contractual funding obligations prevent us from doing so at this time. We are working on offering a solution, once the paper is accepted.
