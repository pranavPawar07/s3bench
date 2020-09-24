Clone the repo.
git clone -b data_verification_tool https://github.com/Seagate/s3bench/

Build the code.
go build (this gives binary file s3bench, run this binary as follows)

Note: If go is not installed, follow below steps to install "go"
    wget https://golang.org/dl/go1.15.2.linux-amd64.tar.gz
    tar -C /usr/local -xzf go1.15.2.linux-amd64.tar.gz
    export PATH=$PATH:/usr/local/go/bin

Check go version as : go version
Expected output : go version go1.15.2 linux/amd64

Run s3bench as follows. 
./s3bench -accessKey <access_key> -accessSecret <access_secret> -bucket <bucketname> -endpoint http://s3.seagate.com -numClients 1 -numSamples 3 -objectSize 1Mb -skipCleanup -verbose
Note: specify the accessKey, accessSecret & bucket.

To run the wrapper script.
./data_verify.sh -K <access_key> -S <access_secret> -b <bucketname> -w <workload_type> -i <no. of iterations> -s <no. of samples> -c <no. of clients>
