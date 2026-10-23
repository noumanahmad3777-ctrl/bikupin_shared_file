

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




curl.exe -i -X POST "https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks" -H "Content-Type: application/json" --data-binary "{"query":"Vad ar det for stod","top_k":5}"
HTTP/1.1 422 Unprocessable Content
Date: Fri, 23 Oct 2026 12:17:25 GMT
Content-Type: application/json
Content-Length: 158
Connection: keep-alive

{"detail":[{"type":"json_invalid","loc":["body",1],"msg":"JSON decode error","input":{},"ctx":{"error":"Expecting property name enclosed in double quotes"}}]}curl: (3) URL rejected: Port number was not a decimal number between 0 and 65535
curl: (6) Could not resolve host: ar
curl: (6) Could not resolve host: det
curl: (6) Could not resolve host: for
curl: (3) unmatched close brace/bracket in position 13:
stod,top_k:5}
            ^
PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2>






curl.exe -i -X POST "https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks" -H "Content-Type: application/json" --data-binary "{\"query\":\"Vad ar det for stod\",\"top_k\":5}"
