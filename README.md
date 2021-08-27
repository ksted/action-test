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
- Actual result: Job 3 runs and fails

## Test 4
- Job 1 is a matrix; one job fails, the other succeeds
- Job 2 requires job 1
- Job 2 succeeds
- Job 3 requires jobs 1 and 2
- Job 3 checks job 1 result
- Expected result: Job 3 runs and fails
- Actual result: Job 3 runs and fails

## Test 5
- Job 1 is a matrix; both jobs succeed
- Job 2 requires job 1
- Job 2 succeeds
- Job 3 requires jobs 1 and 2
- Job 3 checks job 1 result
- Expected result: Job 3 runs and succeeds
- Actual result: Job 3 is skipped

## Test 6
- Job 1 is a matrix; both jobs succeed
- Job 2 requires job 1
- Job 2 succeeds
- Job 3 requires jobs 1 and 2
- Job 3 checks job 1 result
- Job 4 checks job 3 result
- Expected result: Job 4 runs and succeeds
