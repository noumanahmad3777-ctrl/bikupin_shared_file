

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






PS C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2> python .\phase3_collect_answers.py --probe
POST https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks
body: {"query": "Vad är det för stöd man kan få för sin jordbruksmark?", "top_k": 5}

Traceback (most recent call last):
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\phase3_collect_answers.py", line 301, in <module>
    main()
    ~~~~^^
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\phase3_collect_answers.py", line 295, in main
    probe()
    ~~~~~^^
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\phase3_collect_answers.py", line 98, in probe
    answer, contexts, raw = client.query(question)
                            ~~~~~~~~~~~~^^^^^^^^^^
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\rag_client.py", line 268, in query
    raw = self._request(cfg.QUERY_METHOD, full, cfg.QUERY_TIMEOUT, json_body=body)
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\rag_client.py", line 196, in _request
    raise RagApiError(
        f"HTTP {resp.status_code} from {method} {url} :: {resp.text[:300]}",
        status_code=resp.status_code, body=resp.text[:300])
rag_client.RagApiError: HTTP 500 from POST https://sandbox-nahma-bikupan-data-query.tt.tuv.jordbruksverket.se/chunks :: Internal Server Error
