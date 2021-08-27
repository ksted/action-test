# action-test

## Test 1
- Job 1 fails
- Job 2 succeeds
- Expected result: Job 3 runs
- Actual result: Job 3 skipped

## Test 2
- Job 1 fails
- Job 2 succeeds
- Job 3 requires jobs 1 and 2
- Expected result: Job 3 runs
- Actual result: Job 3 runs

## Test 3
- Job 1 fails
- Job 2 succeeds
- Job 3 requires jobs 1 and 2
- Job 3 checks job 1 result
- Expected result: Job 3 runs and fails
