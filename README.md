## Hydra evaluation results

This page presents the detailed results of the evaluation of the XSS prototype of Hydra, a feedback-driven approach for the dynamic exploitation of injection vulnerabilities.

## WAVSEP

Test case | Polyglot successful? | Best context weight (dynamic) | Best context name (dynamic) | # Requests (dynamic) | Best context weight (static) | Best context name (dynamic) | # Requests (static)
-------- | -------- | -------- | -------- | -------- | -------- | -------- | -------- 
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case01_Tag2HtmlPageScope_jsp_userinput_myinputvalue | yes | 100 | Text node in SCRIPT | 2 | 100 | Text node in STYLE | 2
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case02_Tag2TagScope_jsp_userinput_myinputvalue | yes | 50 | Text node in TEXTAREA | 91 | 50 | Text node in TEXTAREA | 2165
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case03_Tag2TagStructure_jsp_userinput_myinputvalue | yes | 100 | Attribute value in INPUT onclick | 29 | 50 | Attribute value in INPUT value | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case04_Tag2HtmlComment_jsp_userinput_myinputvalue | yes | 100 | Text node in SCRIPT | 31 | 100 | Text node in SCRIPT | 3
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case05_Tag2Frameset_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case06_Event2TagScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in IMG src | 1 | 100 | Attribute value in IMG src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case07_Event2DoubleQuotePropertyScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in IMG src | 1 | 100 | Attribute value in IMG src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case08_Event2SingleQuotePropertyScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in IMG src | 1 | 100 | Attribute value in IMG src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case09_SrcProperty2TagStructure_jsp_userinput_myinputvalue | no | 100 | Attribute value in SCRIPT onload | 163 | 50 | Attribute value in SCRIPT id | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case10_Js2DoubleQuoteJsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case11_Js2SingleQuoteJsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case12_Js2JsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case13_Vbs2DoubleQuoteVbsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case14_Vbs2SingleQuoteVbsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case15_Vbs2VbsEventScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in INPUT onclick | 1 | 100 | Attribute value in INPUT onclick | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case16_Js2ScriptSupportingProperty_jsp_userinput_myinputvalue_html | yes | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case17_Js2PropertyJsScopeDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case18_Js2PropertyJsScopeSingleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case19_Js2PropertyJsScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case20_Vbs2PropertyVbsScopeDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case21_Vbs2PropertyVbsScope_jsp_userinput_myinputvalue | no | 100 | Attribute value in FRAME src | 1 | 100 | Attribute value in FRAME src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case22_Js2ScriptTagDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case23_Js2ScriptTagSingleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case24_Js2ScriptTag_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case25_Vbs2ScriptTagDoubleQuoteDelimiter_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case26_Vbs2ScriptTag_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case27_Js2ScriptTagOLCommentScope_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case28_Js2ScriptTagMLCommentScope_jsp_userinput_myinputvalue | yes | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case29_Vbs2ScriptTagOLCommentScope_jsp_userinput_myinputvalue | no | 100 | Text node in SCRIPT | 1 | 100 | Text node in SCRIPT | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case30_Tag2HtmlPageScopeMultipleVulnerabilities_jsp_userinput_myinputvalue_userinput2_1234 | yes | 100 | Text node in SCRIPT | 6 | 100 | Text node in STYLE | 2
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Case32_Tag2HtmlPageScopeValidViewstateRequired_jsp_userinput_myinputvalue_VIEWSTATE_2FwEPDwUENTM4MWRkhsjF_2B62gWnhYUcEyuRwTHxGDVzA_3D | yes |  | 2 | 2 |  |  | 
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case01_Tag2HtmlPageScope_StripScriptTag_jsp_userinput_myinputvalue | yes | 100 | Text node in STYLE | 264 | 100 | Text node in STYLE | 2
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case02_Tag2HtmlPageScope_SecretVectorPOST_jsp_userinput_myinputvalue | no |  | 1 |  |  |  | 
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case03_Tag2HtmlPageScope_ConstantAntiCSRFToken_jsp_anticsrf_0_6790930077575053_userinput_myinputvalue | no |  | 1 |  |  |  | 
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case05_ScriptlessInjectionInFormTagActionAttribute_jsp_userinput_myinputvalue | no | 100 | Attribute value in FORM action | 1 | 100 | Attribute value in FORM action | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case06_ScriptlessInjectionInBaseTagHrefAttribute_jsp_userinput_myinputvalue | no | 100 | Attribute value in BASE href | 1 | 100 | Attribute value in BASE href | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case07_ScriptlessInjectionInScriptTagSrcAttribute_jsp_userinput_myinputvalue | no | 100 | Attribute value in SCRIPT src | 1 | 100 | Attribute value in SCRIPT src | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case08_InjectionInToCssSelector_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case09_InjectionInToCssSelectorAttributeName_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case10_InjectionInToCssProperty_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1
active_Reflected_XSS_RXSS_Detection_Evaluation_GET_Experimental_Case11_InjectionInToCssPropertyValue_jsp_userinput_myinputvalue | no | 100 | Text node in STYLE | 1 | 100 | Text node in STYLE | 1

