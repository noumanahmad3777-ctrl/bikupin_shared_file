

$env:GOLDEN_DATASET  = "..\golden_dataset_sv.json"
$env:TEST_DATASET    = "..\golden_dataset_sv_test.json"
$env:EVAL_OUTPUT_DIR = "..\output\sv"
python .\phase1_prepare_dataset.py


python .\phase3_collect_answers.py --probe


python .\verify_ingestion.py --query-check



$env:GOLDEN_DATASET  = ".\golden_dataset_sv.json"
$env:TEST_DATASET    = ".\golden_dataset_sv_test.json"
$env:EVAL_OUTPUT_DIR = "..\output\sv"
python .\phase1_prepare_dataset.py


$env:GOLDEN_DATASET = "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\golden_dataset_sv.json"
