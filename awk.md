
The Lazy Programmer
===================

## AWK

**Good for**: Extracting data/information from Logfiles

**Example**: Get the name of all test methods and sort them alphabetically:

    $ awk '/function test/' ContractsOperationTest.php | sort
    public function testGetLastDayToCancel()
    public function testGetNextPossibleContractEffectDate()
    public function testInvalidateEndfixedContracts()
    public function testInvalidateSeasonticketContracts()

    ...


**Example**: Check for free diskspace on a partition, exit with error if beyond threshold:

    df | awk '/\/dev\/sda1/ {gsub(/%/,""); if($5 >=75) {print "Disk usage > 75%"; err=1} else {err=0}} END {exit err}'


