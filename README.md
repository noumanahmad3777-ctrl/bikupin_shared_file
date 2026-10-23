

$env:GOLDEN_DATASET  = "..\golden_dataset_sv.json"
$env:TEST_DATASET    = "..\golden_dataset_sv_test.json"
$env:EVAL_OUTPUT_DIR = "..\output\sv"
python .\phase1_prepare_dataset.py


python .\phase3_collect_answers.py --probe


python .\verify_ingestion.py --query-check



PS C:\Users\NAHMA\bikupan> helm install bikupan ./helm
level=ERROR msg="cluster reachability check failed: kubernetes cluster unreachable: the server has asked for the client to provide credentials"                   
Error: INSTALLATION FAILED: cluster reachability check failed: kubernetes cluster unreachable: the server has asked for the client to provide credentials         
PS C:\Users\NAHMA\bikupan> c   



ssh kubernetes@kubeuser.intern.jordbruksverket.se genuser > $HOME/.kube/config




**PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2>
PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2> Invoke-RestMethod -Uri "https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks" -Method Post -ContentType "application/json" -Body '{"query":"Vad ar det for stod","top_k":5}'
Invoke-RestMethod : Internal Server Error
At line:1 char:1
+ Invoke-RestMethod -Uri "https://sandbox-nahma-bikupan-data-query.tt.t ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) [Invoke-RestMethod], WebExc
   eption
    + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeRestMethodCommand
PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2> $body = '{"query":"Vad är det för stöd man kan få för sin jordbruksmark?","top_k":5}' Invoke-RestMethod -Uri "https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks" -Method Post -ContentType "application/json; charset=utf-8" -Body ([System.Text.Encoding]::UTF8.GetBytes($body))
At line:1 char:87
+ ...  kan få för sin jordbruksmark?","top_k":5}' Invoke-RestMethod -Uri "h ...
+                                                 ~~~~~~~~~~~~~~~~~
Unexpected token 'Invoke-RestMethod' in expression or statement.
    + CategoryInfo          : ParserError: (:) [], ParentContainsErrorRecordException
    + FullyQualifiedErrorId : UnexpectedToken

PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2> Invoke-RestMethod -Uri "https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks" -Method Post -ContentType "application/json" -Body '{"query":"What kind of support can you get for farmland?","top_k":5}'
Invoke-RestMethod : Internal Server Error
At line:1 char:1
+ Invoke-RestMethod -Uri "https://sandbox-nahma-bikupan-data-query.tt.t ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (System.Net.HttpWebRequest:HttpWebRequest) [Invoke-RestMethod], WebExc
   eption
    + FullyQualifiedErrorId : WebCmdletWebResponseException,Microsoft.PowerShell.Commands.InvokeRestMethodCommand
PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2>**
