Clone the repo .
git clone https://github.com/Seagate/s3bench/tree/data_verification_tool

Build the code – 
go build (this gives binary file "s3bench", run this binary as follows)

Run ./s3bench -accessKey abcd -accessSecret abcd -bucket abcd -endpoint http://s3.seagate.com -numClients 1 -numSamples 3 -objectSize 1Mb -skipCleanup -verbose 

./data_verify.sh -K <access_key> -S <access_secret> -b <bucketname> -w <workload_type> -i <no. of iterations> -s <no. of samples> -c <no. of clients>  (to run wrapper script)
