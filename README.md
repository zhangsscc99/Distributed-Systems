# distributed system
This is a cloned repository from MIT's distributed system course

#### Project Structure:
This project uses Go Programming Language
Following is the project directory structure:
```
├── go.mod
├── LICENSE
├── Makefile
├── README.md
└── src
    ├── kvraft
    ├── labgob
    ├── labrpc
    ├── main
    ├── models
    ├── mr
    ├── mrapps
    ├── porcupine
    ├── raft
    ├── shardkv
    └── shardmaster
```
This project is added with `go.mod` file. Therefore no need to set `GOPATH` for this project.
Simply clone the repository and following test run should pass.

Check more on Go Module (https://github.com/golang/go/wiki/Modules#faqs--gomod-and-gosum)

#### Using Map Reduce Application:

Testing word count application
    
    [new terminal]
    1. cd main
    2. go build -buildmode=plugin ../mrapps/wc.go && go run mrmaster.go pg-*.txt
    
    [another terminal]
    1. cd main
    2. go run mrworker.go wc.so
    
Testing all the application inside /mrapps/
    
    1. sh ./test-mr.sh

#### Using the Raft application:

    1. cd raft
    2. go test run 2A / 2B or 2C

#### Demo:

![Map reduce & Raft Demo](https://github.com/ddeka0/distributed-system/blob/master/demo-v0.1.gif)
    
