---
id: pulsar-2.8.2
title: Apache Pulsar 2.8.2 
sidebar_label: Apache Pulsar 2.8.2 
---

#### 2021-12-20

### Security
- Upgrade to Log4J 2.17.0 to mitigate CVE-2021-45105 [#13392](https://github.com/apache/pulsar/pull/13392)
- Upgrade Netty to 4.1.72 - CVE-2021-43797 [#13328](https://github.com/apache/pulsar/pull/13328)
- Bump log4j to 2.15.0 [#13226](https://github.com/apache/pulsar/pull/13226)
- Revert new AuthorizationProvider method [#13133](https://github.com/apache/pulsar/pull/13133)
- Support CLEAR_BACKLOG namespace op after enable auth [#12963](https://github.com/apache/pulsar/pull/12963)
- Upgrade netty to 4.1.68.Final [#12218](https://github.com/apache/pulsar/pull/12218)
- Support disabling non-TLS service ports [#11681](https://github.com/apache/pulsar/pull/11681)
- Upgrade Jetty to 9.4.43.v20210629 [#11660](https://github.com/apache/pulsar/pull/11660)

### Broker
- Fix and improve topic ownership assignment [#13069](https://github.com/apache/pulsar/pull/13069)
- Fix LeaderElectionService.getCurrentLeader and add support for empheralOwner in MockZooKeeper [#13066](https://github.com/apache/pulsar/pull/13066)
- Do not reuse the Failed OpAddEntry object which leads to the bundle unloading timeout. [#12993](https://github.com/apache/pulsar/pull/12993)
- Remove readerCaches and close reader when exception occurs in SystemTopicBasedTopicPoliciesService [#12873](https://github.com/apache/pulsar/pull/12873)
- Fix TopicPoliciesCacheNotInitException issue. [#12773](https://github.com/apache/pulsar/pull/12773)
- Support UNSUBSCRIBE namespace op after enabling auth [#12742](https://github.com/apache/pulsar/pull/12742)
- Fix race condition in PersistentTopic#addReplicationCluster [#12729](https://github.com/apache/pulsar/pull/12729)
- Even if always compatible is set, consumers cannot be created [#12721](https://github.com/apache/pulsar/pull/12721)
- Fix the incorrect total size when BrokerEntryMetadata is enabled [#12714](https://github.com/apache/pulsar/pull/12714)
- Fix lost compaction data due to compaction properties missed during reset-cursor [#12698](https://github.com/apache/pulsar/pull/12698)
- Fix TestRunMain test [#12675](https://github.com/apache/pulsar/pull/12675)
- Support GET_METADATA topic op after enabling auth [#12656](https://github.com/apache/pulsar/pull/12656)
- Fix false positive ownership check in OwnershipCache#checkOwnership [#12650](https://github.com/apache/pulsar/pull/12650)
- Optimize exception information for schemas [#12647](https://github.com/apache/pulsar/pull/12647)
- Add @Test annotation to test methods [#12640](https://github.com/apache/pulsar/pull/12640)
- Support retry when creating reader of Topic Policies [#12622](https://github.com/apache/pulsar/pull/12622)
- Fix String should use equals but not ==. [#12619](https://github.com/apache/pulsar/pull/12619)
- Fix 12614, waitingForPingResponse needs to be modified with volatile for concurrent sence  [#12615](https://github.com/apache/pulsar/pull/12615)
- Cleanup ProxyPublishConsumeTest [#12607](https://github.com/apache/pulsar/pull/12607)
- Avoid passing OpAddEntry across a thread boundary in asyncAddEntry [#12606](https://github.com/apache/pulsar/pull/12606)
- Do not move the non-durable cursor position when trimming ledgers while topic with compaction [#12602](https://github.com/apache/pulsar/pull/12602)
- Allow `GetTopicsOfNamespace` op with `consume` permission [#12600](https://github.com/apache/pulsar/pull/12600)
- Allow configuring schema compatibility policy for system topics [#12598](https://github.com/apache/pulsar/pull/12598)
- Cleanup already deleted namespace topics. [#12597](https://github.com/apache/pulsar/pull/12597)
- Fix additional servlets NAR might extract to null directory [#12585](https://github.com/apache/pulsar/pull/12585)
- Fix log typo in NamespaceService#checkHeartbeatNamespace  [#12582](https://github.com/apache/pulsar/pull/12582)
- Add OpAddEntry to pendingAddEntries after the state check [#12570](https://github.com/apache/pulsar/pull/12570)
- Cancel scheduled tasks when deleting ManagedLedgerImpl [#12565](https://github.com/apache/pulsar/pull/12565)
- Add git branch information for PulsarVersion [#12541](https://github.com/apache/pulsar/pull/12541)
- Websocket should pass the encryption context to consumers [#12539](https://github.com/apache/pulsar/pull/12539)
- The count of topics on the bundle is less than 2，skip split [#12527](https://github.com/apache/pulsar/pull/12527)
- Fix the reader skips compacted data which original ledger been removed [#12522](https://github.com/apache/pulsar/pull/12522)
- Fix `messageDedup` delete inactive producer name [#12493](https://github.com/apache/pulsar/pull/12493)
- Optimize the code: remove extra spaces [#12470](https://github.com/apache/pulsar/pull/12470)
- Future completed twice in the method of  impl.MLPendingAckStore#closeAsync [#12362](https://github.com/apache/pulsar/pull/12362)
- Fix the race of delete subscription and delete topic [#12240](https://github.com/apache/pulsar/pull/12240)
- Disable stats recorder for built-in PulsarClient [#12217](https://github.com/apache/pulsar/pull/12217)
- Fix delete authentication policies when deleting topics. [#12215](https://github.com/apache/pulsar/pull/12215)
- Optimize the memory usage of Cache Eviction [#12045](https://github.com/apache/pulsar/pull/12045)
- Avoid adding duplicated BrokerEntryMetadata [#12018](https://github.com/apache/pulsar/pull/12018)
- Fix update ledger list to znode version mismatch failed, ledger not delete [#12015](https://github.com/apache/pulsar/pull/12015)
- Fix messages in TopicPolicies will never be cleaned up [#11928](https://github.com/apache/pulsar/pull/11928)
- Fix returned wrong hash ranges for the consumer with the same consumer name [#12212](https://github.com/apache/pulsar/pull/12212)
- Add Key_Shared metadata to topic stats [#11839](https://github.com/apache/pulsar/pull/11839)
- Fix build from submodules (broker, transaction coordinator) [#11795](https://github.com/apache/pulsar/pull/11795)
- Add method to clear up transaction buffer snapshot [#11934](https://github.com/apache/pulsar/pull/11934)
- Increase the test stability of transactionTest [#11541](https://github.com/apache/pulsar/pull/11541)
- Add maven.restlet.org repository [#13248](https://github.com/apache/pulsar/pull/13248)
- Fix and improve topic ownership assignment (#13069) [#13117](https://github.com/apache/pulsar/pull/13117)
- Evaluate the current protocol version once [#13045](https://github.com/apache/pulsar/pull/13045)
- Revert "Set default root log level to debug" and make PULSAR_LOG_ROOT_LEVEL default to PULSAR_LOG_LEVEL [#12941](https://github.com/apache/pulsar/pull/12941)
- Catch exceptions in scheduled tasks to prevent unintended cancellation [#12853](https://github.com/apache/pulsar/pull/12853)
- Fix producer getting incorrectly removed from topic's `producers` map [#12846](https://github.com/apache/pulsar/pull/12846)
- Synchronize updates to the inactiveProducers map in MessageD… [#12820](https://github.com/apache/pulsar/pull/12820)
- Close connection after receiving unexpected SendCommand [#12780](https://github.com/apache/pulsar/pull/12780)
- Fix namespace policy override ignored when creating subscription [#12699](https://github.com/apache/pulsar/pull/12699)
- Update lombok to 1.18.22 [#12466](https://github.com/apache/pulsar/pull/12466)
- Fix skips compacted data for reader/consumer [#12464](https://github.com/apache/pulsar/pull/12464)
- Remove data race in MultiTopicsConsumerImpl to ensure correct message order [#12456](https://github.com/apache/pulsar/pull/12456)
- Fix the retry topic's `REAL_TOPIC` & `ORIGIN_MESSAGE_ID` property [#12451](https://github.com/apache/pulsar/pull/12451)
- Change the producer fence error log to debug level [#12447](https://github.com/apache/pulsar/pull/12447)
- Reduce the readFailureBackoff time [#12444](https://github.com/apache/pulsar/pull/12444)
- Fix wrong property name in NamespaceIsolationDataImpl#secondary [#12433](https://github.com/apache/pulsar/pull/12433)
- Optimize SecurityUtility code flow [#12431](https://github.com/apache/pulsar/pull/12431)
- Fix compactor skips data from last compacted Ledger [#12429](https://github.com/apache/pulsar/pull/12429)
- Remove redundant code [#12424](https://github.com/apache/pulsar/pull/12424)
- Fix some tests not enabled in integration tests [#12417](https://github.com/apache/pulsar/pull/12417)
- Use weak ref to ClientConnection for timeout task [#12409](https://github.com/apache/pulsar/pull/12409)
- Fix cherry-pick issue [#12397](https://github.com/apache/pulsar/pull/12397)
- Fix the null point caused by deleting the system topic policy [#12367](https://github.com/apache/pulsar/pull/12367)
- Update delete inactive topic configuration documentation [#12350](https://github.com/apache/pulsar/pull/12350)
- Add log to print exception stack. [#12345](https://github.com/apache/pulsar/pull/12345)
- Avoid potentially blocking calls to metadata on critical threads [#12339](https://github.com/apache/pulsar/pull/12339)
- Fix NPE when removing cursor [#12297](https://github.com/apache/pulsar/pull/12297)
- Print log when configuration is failed to load [#12280](https://github.com/apache/pulsar/pull/12280)
- Fix incorrect returned last message ID while the `lastConfirmedEntry` with negative entry ID [#12277](https://github.com/apache/pulsar/pull/12277)
- Fix TTL expiry does not take effect [#12266](https://github.com/apache/pulsar/pull/12266)
- The loadbalancer should avoid offload the heartbeat namespace [#12252](https://github.com/apache/pulsar/pull/12252)
- Fix typo of the returned last message ID when the last message ID is from compacted ledger [#12237](https://github.com/apache/pulsar/pull/12237)
- Add support for splitting topics and partition labels in Prometheus [#12225](https://github.com/apache/pulsar/pull/12225)
- Fix lost message issues 12221 [#12223](https://github.com/apache/pulsar/pull/12223)
- Allow to config pulsar client allocator out of memory policy [#12200](https://github.com/apache/pulsar/pull/12200)
- Remove redundant parameters [#12188](https://github.com/apache/pulsar/pull/12188)
- Fix incorrect logger numbers in tests [#12168](https://github.com/apache/pulsar/pull/12168)
- Return the last position of the compacted data while the original data has been deleted [#12161](https://github.com/apache/pulsar/pull/12161)
- Improve exceptions thrown when handling the schema resource [#12155](https://github.com/apache/pulsar/pull/12155)
- Fix prefix setting in JWT authn and avoid multi calls for the getProperty [#12132](https://github.com/apache/pulsar/pull/12132)
- Fix used after recycle issue in OpAddEntry [#12103](https://github.com/apache/pulsar/pull/12103)
- Bugfix: Fix rackaware placement policy init error [#12097](https://github.com/apache/pulsar/pull/12097)
- Fix wrong key-hash selector used for new consumers after all the previous consumers disconnected [#12035](https://github.com/apache/pulsar/pull/12035)
- Fix cherry-pick issue on branch-2.8 [#11982](https://github.com/apache/pulsar/pull/11982)
- Remove unused variable and unnecessary box in NamespaceBundleFactory [#11975](https://github.com/apache/pulsar/pull/11975)
- Print position info when can't find next valid position. [#11969](https://github.com/apache/pulsar/pull/11969)
- Fix NPE ZkBookieRackAffinityMapping [#11947](https://github.com/apache/pulsar/pull/11947)
- Avoid to infinitely split bundle [#11937](https://github.com/apache/pulsar/pull/11937)
- Improved logic for pausing replicated subscription snapshots when no traffic [#11922](https://github.com/apache/pulsar/pull/11922)
- Fix ZKSessionTest.testReacquireLocksAfterSessionLost [#11886](https://github.com/apache/pulsar/pull/11886)
- Schema compatibility strategy in broker level. [#11856](https://github.com/apache/pulsar/pull/11856)
- Use TestRetrySupport for BaseMetadataStoreTests to cleanup state between retries [#11771](https://github.com/apache/pulsar/pull/11771)
- Remove replace_maven-wagon-http-version.sh script [#11718](https://github.com/apache/pulsar/pull/11718)
- Check null or empty instead of catch NPE [#11655](https://github.com/apache/pulsar/pull/11655)
- Avoid duplicate deletion of schema [#11640](https://github.com/apache/pulsar/pull/11640)
- Fix subscribeRateLimiter cannot be disabled [#11614](https://github.com/apache/pulsar/pull/11614)
- Fix race condition in concurrent schema deletion [#11606](https://github.com/apache/pulsar/pull/11606)
- Use `get` instead of `join` to avoid getting stuck [#11597](https://github.com/apache/pulsar/pull/11597)
- Avoid to cal getMaximumRolloverTimeMs everytime [#11513](https://github.com/apache/pulsar/pull/11513)
- Fix improper class/method/field modifiers [#10837](https://github.com/apache/pulsar/pull/10837)
- Support max-connection and max-connection-per-IP [#10754](https://github.com/apache/pulsar/pull/10754)
- Allow Integration Tests Jar to be deployed to Maven central [#12292](https://github.com/apache/pulsar/pull/12292)

### Functions
- K8s runtime: force deletion to avoid hung function worker during connector restart [#12504](https://github.com/apache/pulsar/pull/12504)
- Fix k8s pulsar functions containers not exposing metrics port for scraping [#12065](https://github.com/apache/pulsar/pull/12065)
- Enable protobuf-native schema support for function [#11868](https://github.com/apache/pulsar/pull/11868)
- Pass `SubscriptionPosition` from `FunctionDetails` to `FunctionConfig` / `SinkConfig` [#11831](https://github.com/apache/pulsar/pull/11831)
- Reorganize the context hierarchy for functions [#10631](https://github.com/apache/pulsar/pull/10631)
- Remove the deprecated API usage in HDFS [#12080](https://github.com/apache/pulsar/pull/12080)
- Stop OffsetStore when stopping the connector [#12457](https://github.com/apache/pulsar/pull/12457)
- Support set subscription position [#11990](https://github.com/apache/pulsar/pull/11990)
- Sync to the latest function proto [#11853](https://github.com/apache/pulsar/pull/11853)
- Fix classloader leaks [#12973](https://github.com/apache/pulsar/pull/12973)
- Add missing dependency [#12246](https://github.com/apache/pulsar/pull/12246)
- ConcurrentHashMap should be used for caching producers [#11820](https://github.com/apache/pulsar/pull/11820)
- Support KEY_BASED batch builder for Java based functions and sources [#11706](https://github.com/apache/pulsar/pull/11706)

### Pulsar Admin
- Print topic internal info as formatted JSON [#12709](https://github.com/apache/pulsar/pull/12709)
- Fix last exit code storage [#12581](https://github.com/apache/pulsar/pull/12581)
- Fix the issue of failing to update partitions of topics [#11683](https://github.com/apache/pulsar/pull/11683)
- Perfect judgment conditions of pulsar-admin [#12315](https://github.com/apache/pulsar/pull/12315)
- Fix log level config for pulsar-admin, pulsar-client and pulsar-perf [#12915](https://github.com/apache/pulsar/pull/12915)
- Modify exception of set-properties for namespace [#12436](https://github.com/apache/pulsar/pull/12436)
- Get schema validation enforce add applied [#12349](https://github.com/apache/pulsar/pull/12349)

### Tiered Storage
- Add retry to tolerate the offload index file read failure [#12452](https://github.com/apache/pulsar/pull/12452)
- Fix the read performance issue in the offload readAsync [#12443](https://github.com/apache/pulsar/pull/12443)
- Fix FileSystemManagedLedgerOffloader can not clean up outdated ledger [#12309](https://github.com/apache/pulsar/pull/12309)
- Fix the potential race condition in the BlobStore readhandler [#12123](https://github.com/apache/pulsar/pull/12123)

### Pulsar SQL
- Handle message null schema version in PulsarRecordCursor [#12809](https://github.com/apache/pulsar/pull/12809)
- Pulsar SQL support query big entry data [#12448](https://github.com/apache/pulsar/pull/12448)

### CLI
- Enable CLI to publish non-batched messages [#12641](https://github.com/apache/pulsar/pull/12641)
- Make it possible to disable poolMessages [#12108](https://github.com/apache/pulsar/pull/12108)
- Add total messages when periodic printing throughput [#12084](https://github.com/apache/pulsar/pull/12084)
- Make it possible to disable poolMessages [#12090](https://github.com/apache/pulsar/pull/12090)

### Unit Test
- Broker resource group test optimize fail msg [#12438](https://github.com/apache/pulsar/pull/12438)
- Fix windows test path problem [#12398](https://github.com/apache/pulsar/pull/12398)
- Make AuthenticationTokenTest to run on windows [#12329](https://github.com/apache/pulsar/pull/12329)
- Use correct line separator instead of \n [#12143](https://github.com/apache/pulsar/pull/12143)

### BookKeeper
- Add readWorkerThreadsThrottlingEnabled to conf/bookkeeper.conf [#12666](https://github.com/apache/pulsar/pull/12666)
- UseV2WireProtocol for bookkeeper autorecovery [#12311](https://github.com/apache/pulsar/pull/12311)

### Proxy
- Reduce the severity of log "refreshing key manager" in KeyManagerProxy [#12594](https://github.com/apache/pulsar/pull/12594)
- Set default HTTP proxy request timeout [#11971](https://github.com/apache/pulsar/pull/11971)
- Set default httpProxyTimeout to 5 minutes [#12299](https://github.com/apache/pulsar/pull/12299)
- Fix Pulsar Proxy to re-use authentication instance [#12245](https://github.com/apache/pulsar/pull/12245)
- Fix NPE in ProxyConnection with no auth data [#12111](https://github.com/apache/pulsar/pull/12111)
- Fix ProxyConnection to check for existence of auth_data field [#12057](https://github.com/apache/pulsar/pull/12057)