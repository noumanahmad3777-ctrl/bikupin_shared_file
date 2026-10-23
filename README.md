

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




https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/docs#/default/query_endpoint_query_post
