

$env:GOLDEN_DATASET  = "..\golden_dataset_sv.json"
$env:TEST_DATASET    = "..\golden_dataset_sv_test.json"
$env:EVAL_OUTPUT_DIR = "..\output\sv"
python .\phase1_prepare_dataset.py


python .\phase3_collect_answers.py --probe


python .\verify_ingestion.py --query-check



Traceback (most recent call last):
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\phase1_prepare_dataset.py", line 89, in <module>
    main()
    ~~~~^^
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\phase1_prepare_dataset.py", line 85, in main
    prepare(args.golden, args.out, args.dry_run)
    ~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\phase1_prepare_dataset.py", line 47, in prepare
    records = dataset_io.load_records(golden_path)
  File "C:\Users\NAHMA\gpu-helm-test\bikupan\ragas_demo\evaluation\test_v2\dataset_io.py", line 16, in load_records
    with open(path, encoding="utf-8") as fh:
         ~~~~^^^^^^^^^^^^^^^^^^^^^^^^
FileNotFoundError: [Errno 2] No such file or directory: '..\\golden_dataset_sv.json'
