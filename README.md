#Maelstrom binary and its jar file present under maelstorm folder
#created seperate folder for each problem.

Folder Structure
```
.
├── README.md
├── echo (1st Problem code)
│   ├── api
│   │   ├── __init__.py
│   │   ├── __pycache__
│   │   │   ├── __init__.cpython-311.pyc
│   │   │   └── errors.cpython-311.pyc
│   │   └── errors.py
│   └── echo.py
├── go (Sample code to test maelstrom)
│   └── main.go (echo code)
├── maelstrom (binary)
│   ├── lib
│   │   └── maelstrom.jar
│   └── maelstrom
├── challange_1.py (echo problem solution)
├── challange_2.py (unique id generation solution)
├── challange_3.py (broadcat solution)
```

```
How to execute the programs?
1. Challange 1 - Echo
    - clone the repo
    - switch to clone repo drirectory
    - ./maelstorm/maelstrom test -w echo \
        --bin ./challange_1.py \
        --node-count 1 \
        --time-limit 10
2. Challange 2 - Unique ID Generation
    - clone the repo
    - switch to clone repo drirectory
    - ./maelstorm/maelstrom test 
        -w unique-ids 
        --bin ./challange_2.py \
        --time-limit 30 \
        --rate 1000 \
        --node-count 3 \
        --availability total \
        --nemesis partition
3. Challange 3 - Broadcast
    - clone the repo
    - switch to clone repo drirectory
    - ./maelstorm/maelstrom test --workload broadcast \
        --bin challange_3.py \
        --node-count 5 \
        --time-limit 20 \
        --rate 10
```

Solution Output 
challange 1 | refer file output_challange1.md
challange 2 | refer file output_challange2.md
challange 3 | refer file output_challange3.md







