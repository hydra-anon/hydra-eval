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

The following table details which of the evaluated tools was able to exploit the respective SUT.

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


The following table shows the minimum and maximum number of requests required by each of the evaluated solutions to exploit the given SUT. Note that the XSS polyglot shortcut will always require exactly two requests if it is successful (one to determine the current output context, one to inject the shortcut).

ID  | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------
B01 | 2 | 2 | 2 | 5-6 | 69
B02 | 2 | ✕ | ✕ | 5-6 | ✕
B03 | 2 | 20-29 | ✕ | 5-7 | 75
B04 | 2 | 25-34 | 3-4 | 5-7 | 69
B05 | ✕ | 1 | 1 | 5-9 | 190-211
B06 | ✕ | 1 | 1 | 15-16 | 76
B07 | ✕ | 1 | 1 | 15-17 | 76
B08 | ✕ | 1 | 1 | 15-17 | ✕
B09 | ✕ | 132-191 | ✕ | 15-17 | 88
B10 | ✕ | 1 | 1 | 15-18 | 81
B11 | ✕ | 1 | 1 | 15-17 | 81
B12 | ✕ | 1 | 1 | 15-18 | 81
B13 | ✕ | 1 | 1 | 15-17 | 81
B14 | ✕ | 1 | 1 | 15-16 | ✕
B15 | ✕ | 1 | 1 | 15-16 | ✕
B16 | 2 | 1 | 1 | 15-16 | 204
B17 | ✕ | 1 | 1 | 15-17 | 143-144
B18 | ✕ | 1 | 1 | 15-16 | 143
B19 | ✕ | 1 | 1 | 15-17 | 142-144
B20 | ✕ | 1 | 1 | 15-17 | 166-167
B21 | ✕ | 1 | 1 | 15-17 | ✕
B22 | ✕ | 1 | 1 | 15-16 | 81
B23 | ✕ | 1 | 1 | 15-17 | 81
B24 | ✕ | 1 | 1 | 15-17 | 81
B25 | ✕ | 1 | 1 | 15-17 | ✕
B26 | ✕ | 1 | 1 | 15-17 | ✕
B27 | ✕ | 1 | 1 | 15-17 | ✕
B28 | 2 | 1 | 1 | 15-17 | ✕
B29 | ✕ | 1 | 1 | 15-17 | ✕
B30 | 2 | 4-6 | 2 | 6-8 | 108
B31 | ✕ | ✕ | ✕ | 5-7 | ✕
B32 | 2 | ✕ | ✕ | 5-7 | 71
E01 | 2 | 221-280 | 2 | 5-9 | 84-136
E02 | ✕ | ✕ | ✕ | ✕ | ✕
E03 | ✕ | ✕ | ✕ | 16-19 | 75
E04 | ✕ | ✕ | ✕ | ✕ | ✕
E05 | ✕ | 1 | 1 | ✕ | ✕
E06 | ✕ | 1 | 1 | ✕ | ✕
E07 | ✕ | 1 | 1 | ✕ | ✕
E08 | ✕ | 1 | 1 | 15-18 | ✕
E09 | ✕ | 1 | 1 | 15-18 | ✕
E10 | ✕ | 1 | 1 | 15-19 | ✕
E11 | ✕ | 1 | 1 | 15-18 | ✕

## Firing Range

The following table details which of the evaluated tools was able to exploit the respective SUT.

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


The following table shows the minimum and maximum number of requests required by each of the evaluated solutions to exploit the given SUT. Note that the XSS polyglot shortcut will always require exactly two requests if it is successful (one to determine the current output context, one to inject the shortcut).

ID  | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------
F1 | ✕ | 1 | 1 | 15-56 | ✕
F2 | 2 | 1 | 1 | 15-26 | ✕
F3 | 2 | 1 | 1 | 15 | ✕
F4 | 2 | 1-30 | 1-4 | 4-36 | 69-180
F5 | 2 | 2-418 | 2-3 | 4-5 | 75
F6 | 2 | 1-10 | 1 | 4-15 | 69-124
F7 | 2 | 1 | 1 | 4-15 | 75-85
F8 | 2 | 1-7 | 1-6 | 4-15 | 69-88
F9 | 2 | 2-290 | 2 | 4-15 | 82
F10 | ✕ | ✕ | ✕ | ✕ | ✕
F11 | ✕ | ✕ | ✕ | 15 | ✕
F12 | ✕ | ✕ | ✕ | ✕ | ✕
F13 | ✕ | ✕ | ✕ | 15 | ✕
F14 | ✕ | ✕ | ✕ | ✕ | ✕
F15 | ✕ | ✕ | ✕ | 15 | ✕
F16 | ✕ | ✕ | ✕ | ✕ | ✕
F17 | ✕ | ✕ | ✕ | 15 | ✕
F18 | ✕ | ✕ | ✕ | ✕ | ✕
F19 | ✕ | 1 | 1 | 56 | ✕
F20 | ✕ | 1 | 1 | ✕ | ✕
F21 | ✕ | 1 | 1 | 26 | ✕
F22 | ✕ | 1 | 1 | ✕ | ✕
F23 | ✕ | 1 | 1 | 15 | ✕
F24 | ✕ | 1 | 1 | ✕ | ✕
F25 | ✕ | 1 | 1 | 15 | ✕
F26 | ✕ | 1 | 1 | ✕ | ✕
F27 | 2 | 1 | 1 | 15 | ✕
F28 | ✕ | 1 | 1 | ✕ | ✕
F29 | 2 | 1 | 1 | 15 | ✕
F30 | ✕ | 1 | 1 | ✕ | ✕
F31 | 2 | 1 | 1 | 15 | ✕
F32 | ✕ | 1 | 1 | ✕ | ✕
F33 | 2 | 1 | 1 | 15 | ✕
F34 | ✕ | 1 | 1 | ✕ | ✕
F35 | 2 | 1 | 1 | 15 | ✕
F36 | ✕ | 1 | 1 | ✕ | ✕
F37 | ✕ | 1 | 1 | 15 | ✕
F38 | ✕ | 1 | 1 | ✕ | ✕
F39 | ✕ | ✕ | ✕ | ✕ | ✕
F40 | ✕ | ✕ | ✕ | ✕ | ✕
F41 | ✕ | ✕ | ✕ | 15 | ✕
F42 | ✕ | ✕ | ✕ | ✕ | ✕
F43 | 2 | 1 | 1 | 15 | 87
F44 | 2 | 1 | 1 | 15 | 87
F45 | 2 | 1 | 1 | 15 | 87
F46 | 2 | 3 | 3 | 35-36 | 180
F47 | 2 | 2 | 3-4 | 5 | 69
F48 | 2 | ✕ | ✕ | 4-5 | 69
F49 | 2 | 20-30 | 3-4 | 4-5 | 69
F50 | 2 | 3-418 | 2 | 4 | 75
F51 | 2 | 5-7 | ✕ | 4 | 75
F52 | 2 | 5-20 | ✕ | 5 | 75
F53 | 2 | 8-22 | ✕ | 4 | 75
F54 | 2 | 8-15 | ✕ | 4-5 | ✕
F55 | 2 | 2 | 2 | 5 | ✕
F56 | 2 | 2 | 2 | 5 | ✕
F57 | 2 | 2 | 2 | 5 | ✕
F58 | 2 | 2 | 2 | ✕ | ✕
F59 | 2 | 2 | 2-3 | ✕ | ✕
F60 | ✕ | ✕ | ✕ | 4-5 | 69
F61 | ✕ | ✕ | ✕ | 5 | 124
F62 | 2 | ✕ | ✕ | 8-9 | ✕
F63 | ✕ | ✕ | ✕ | 4-5 | ✕
F64 | ✕ | ✕ | ✕ | 5 | ✕
F65 | ✕ | 4-10 | ✕ | 5 | ✕
F66 | 2 | 1 | 1 | 13-15 | ✕
F67 | 2 | 1 | 1 | 4-5 | ✕
F68 | 2 | 1 | 1 | 4-5 | ✕
F69 | ✕ | ✕ | ✕ | 15 | 75
F70 | ✕ | ✕ | ✕ | 15 | 75
F71 | ✕ | ✕ | ✕ | 15 | 75
F72 | 2 | 1 | 1 | 4-5 | 85
F73 | 2 | 1 | 1 | 5 | 85
F74 | 2 | 1 | 1 | 5 | 85
F75 | 2 | 1 | 1 | 4 | 85
F76 | 2 | 1 | 1 | 4 | 85
F77 | 2 | 1 | 1 | 4-5 | ✕
F78 | ✕ | 1 | 1 | 4-5 | ✕
F79 | ✕ | 1 | 1 | 14-15 | 80
F80 | ✕ | ✕ | ✕ | 14-15 | 88
F81 | ✕ | 1 | 1 | 14 | ✕
F82 | ✕ | ✕ | ✕ | ✕ | ✕
F83 | ✕ | ✕ | ✕ | ✕ | ✕
F84 | ✕ | ✕ | ✕ | 5 | 69
F85 | ✕ | ✕ | ✕ | 14-15 | 69
F86 | ✕ | ✕ | ✕ | 15 | 69
F87 | ✕ | 2 | 4-6 | 14 | ✕
F88 | ✕ | 6-7 | ✕ | 15 | ✕
F89 | 2 | 2 | 2 | 4-5 | ✕
F90 | 2 | 2 | 2 | 4 | ✕
F91 | ✕ | 44-290 | 2 | 4-5 | ✕

## Juice Shop

The following table details which of the evaluated tools was able to exploit the respective SUT.

ID  | Title | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------ | ------
Juice | Search request/location hash | ✓ | ✕ | ✓ | ✕ | ✕


The following table shows the minimum and maximum number of requests required by each of the evaluated solutions to exploit the given SUT. Note that the XSS polyglot shortcut will always require exactly two requests if it is successful (one to determine the current output context, one to inject the shortcut).

ID  | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------
Juice | 2 | ✕ | 2 | ✕ | ✕

## Real-world applications

The following table details which of the evaluated tools was able to exploit the respective SUT.

ID  | Title | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------ | ------
MyBB | MyBB ModCP finduser | ✓ | ✕ | ✕ | ✕ | ✓
Mara | MaraCMS theme | ✓ | ✓ | ✓ | ✓ | ✓
Tailor | Tailor Login | ✓ | ✓ | ✓ | ✕ | ✓
TL01 | TestLink reqURI | ✓ | ✓ | ✓ | ✕ | ✕
TL02 | TestLink show_mode | ✓ | ✓ | ✓ | ✕ | ✕


The following table shows the minimum and maximum number of requests required by each of the evaluated solutions to exploit the given SUT. Note that the XSS polyglot shortcut will always require exactly two requests if it is successful (one to determine the current output context, one to inject the shortcut).

ID  | HydraShort | Hydra | HydraStatic | w3af | AppScan
------ | ------ | ------ | ------ | ------ | ------
MyBB | 2 | ✕ | ✕ | ✕ | 2
Mara | 2 | 1 | 1 | 10 | 202
Tailor | 2 | 6-8 | 2-3 | ✕ | 88
TL01 | 2 | 1 | 1 | ✕ | ✕
TL02 | 2 | 124-379 | 2-3 | ✕ | ✕

# Additional Material

While we would like to offer a download of the Hydra source code at this time, contractual funding obligations prevent us from doing so at this time. We are working on offering a solution, once the paper is accepted.
