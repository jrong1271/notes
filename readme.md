## Daily Digest

2/15/2025, 10:26:15 PM 

- ### Docker
  - provide an isolated run environment (container) to run app, in bundle dependencies and config, unlike vm, docker container only include necessary libraries, setting and software required to run the apps
    - docker client->server (docker-cli->deamon)
    - docker server=>engine->jobs(1,2,3,4)->runC & container
  - #### Components
    - Base image
    - Dockerfile (todo list)
    - Docker container (process)
    - Docker registry, allow git-like pull from centralized registry from distributed server that are built with docker image
    - NameSpace & Cgroup
  - #### Commands
    - docker build, with dockerfile
    - docker compose 
    - docker pull/push
    - docker run
  - #### Advance
    - docker **compose** up via yaml (db service, authentication service, CMS -container)
    - docker swarm vs k8s, manage container vs pod, managing each pod through api

- ### Redis
  - Redis is a **dictionary service** and a friend for mysql; mysql has a hard limit of 5k QPS, redis is the buffer/caching layer, it store most-frequently-used data in memory and with snapshot stored hard drive for quick recovery, the persistent mechanism is called AOF
  - abandon HTTP and use TCP for speed, and many language has support for redis cli
  - **RedisJSON** vs MongoDB, both use JSON query to read and update data
  - **RedisSearch**(in-memory) VS ES, similar but faster than ElasticSearch (disk-based), but ES has more advanced aggregation and support for large scale project.
  - RedisGraph vs neo, 
  - RedisTimeSeries(in-memory) vs influxDB, process sequential data sorted by time
  
2/13/2025, 11:09:43 PM 
- ### Leetcode problem:
  - #### leafSimiliar
    - compare leafs from two trees
      1. use recursive function
      2. passing two params to recursive functions, tree & lists
      3. if continuation in linked node stop, add value to list
  - #### probductExceptSelf
    - interate from 1 to n, multiple left and right numbers and store product to current
      1. use two for-loops
      2. multiply each number from 0 to n
      3. multiple productOfLeftNums(initially 1) with the above
      4. multiply each number from n to 0
      5. multiply productOfRightNums(initially 1) with the above
  - #### moveZeros
    - iterate from 0 to n, only swap number and increase insertTo(k) index when value is not zero
    - **i and k always point the same number** to prevent unintended swap until zero is found, when zero is found, point k to current index
  - #### compress
    - compress repeating characters with [c, numsOfRepeats...]
      1. use **two pointers**, so we know the number of repeating character
      2. reset pointers to same index only when a different character is found
  - #### increasingTriplet
    - find 3 numbers in ascending order
      1. use **two pointers**, so we have min and middle, when the next number in the loop is bigger than middle, return true


