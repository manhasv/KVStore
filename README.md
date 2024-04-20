# KVStore

High level Approach:
 To implement this project, we followed a simplified RAFT protocol involving multiple replicas with leader who control the states, log of the datastore. The datastore supports two basic API call put and get. 
 The replicas can figure out the message and redirect them if needed, there is a heartbeat system to track the leader activity and fire an election process if inactivity is detected.
Challenges:
 Obviously, the most difficult step was to understand how the RAFT protocol works, I needed to read through the RAFT paper a few times as well as listen to some RAFT videos to fully get it.
 I also had trouble at first on how to established the replicas and leader but it worked out in the end
 The Advance test are hard too.
List of properties/design choices: I implemented a simplied version of RAFT protocol, which includes these features:
 - leader election protocol
 - message redirection
 - updates states based on leader
 - heartbeat
Testing strategy: For testing, I mainly run my local tests with given config files, and make changes accordingly, the last and final insurance should be the test on Gradescope


