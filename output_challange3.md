##Output

###Solution 3

```
pankaj.negi@P2HNYH1W16 maelstrom-problems % ./maelstrom/maelstrom test -w broadcast --bin challange_3.py --node-count 1 --time-limit 20 --rate 10
WARNING: abs already refers to: #'clojure.core/abs in namespace: clojure.core.matrix.impl.mathsops, being replaced by: #'clojure.core.matrix.impl.mathsops/abs
Warning: protocol #'clojure.core.matrix.protocols/PMathsFunctions is overwriting function abs
WARNING: abs already refers to: #'clojure.core/abs in namespace: clojure.core.matrix.protocols, being replaced by: #'clojure.core.matrix.protocols/abs
WARNING: abs already refers to: #'clojure.core/abs in namespace: clojure.core.matrix, being replaced by: #'clojure.core.matrix/abs
WARNING: abs already refers to: #'clojure.core/abs in namespace: clojure.core.matrix.dataset, being replaced by: #'clojure.core.matrix/abs
WARNING: abs already refers to: #'clojure.core/abs in namespace: incanter.core, being replaced by: #'incanter.core/abs
INFO [2024-01-06 15:07:51,658] main - jepsen.cli Test options:
 {:args [],
 :log-net-send false,
 :node-count 1,
 :availability nil,
 :max-txn-length 4,
 :concurrency 1,
 :max-writes-per-key 16,
 :leave-db-running? false,
 :logging-json? false,
 :nemesis-interval 10,
 :log-stderr false,
 :ssh
 {:dummy? false,
  :username "root",
  :password "root",
  :strict-host-key-checking false,
  :private-key-path nil},
 :rate 10.0,
 :argv
 ("test"
  "-w"
  "broadcast"
  "--bin"
  "challange_3.py"
  "--node-count"
  "1"
  "--time-limit"
  "20"
  "--rate"
  "10"),
 :nemesis #{},
 :nodes ["n0"],
 :test-count 1,
 :latency {:mean 0, :dist :constant},
 :bin "challange_3.py",
 :log-net-recv false,
 :time-limit 20,
 :workload :broadcast,
 :consistency-models [:strict-serializable],
 :topology :grid}

INFO [2024-01-06 15:07:51,693] jepsen test runner - jepsen.core Command line:
lein run test -w broadcast --bin challange_3.py --node-count 1 --time-limit 20 --rate 10
INFO [2024-01-06 15:07:51,735] jepsen test runner - jepsen.core Running test:
{:args []
 :remote
 #jepsen.control.retry.Remote{:remote #jepsen.control.scp.Remote{:cmd-remote #jepsen.control.sshj.SSHJRemote{:concurrency-limit 6,
                                                                                                             :conn-spec nil,
                                                                                                             :client nil,
                                                                                                             :semaphore nil},
                                                                 :conn-spec nil},
                              :conn nil}
 :log-net-send false
 :node-count 1
 :availability nil
 :max-txn-length 4
 :concurrency 1
 :db
 #object[maelstrom.db$db$reify__16142
         "0x3c634a04"
         "maelstrom.db$db$reify__16142@3c634a04"]
 :max-writes-per-key 16
 :leave-db-running? false
 :name "broadcast"
 :logging-json? false
 :start-time
 #object[org.joda.time.DateTime "0x10c26161" "2024-01-06T15:07:51.664+05:30"]
 :nemesis-interval 10
 :net
 #object[maelstrom.net$jepsen_net$reify__15251
         "0x1ef6977b"
         "maelstrom.net$jepsen_net$reify__15251@1ef6977b"]
 :client
 #object[maelstrom.workload.broadcast$client$reify__16644
         "0x674cd2da"
         "maelstrom.workload.broadcast$client$reify__16644@674cd2da"]
 :barrier
 #object[java.util.concurrent.CyclicBarrier
         "0x686279e0"
         "java.util.concurrent.CyclicBarrier@686279e0"]
 :log-stderr false
 :pure-generators true
 :ssh {:dummy? true}
 :rate 10.0
 :checker
 #object[jepsen.checker$compose$reify__11881
         "0x6b28d4e4"
         "jepsen.checker$compose$reify__11881@6b28d4e4"]
 :argv
 ("test"
  "-w"
  "broadcast"
  "--bin"
  "challange_3.py"
  "--node-count"
  "1"
  "--time-limit"
  "20"
  "--rate"
  "10")
 :nemesis
 (jepsen.nemesis.ReflCompose
  {:fm {:start-partition 0,
        :stop-partition 0,
        :kill 1,
        :start 1,
        :pause 1,
        :resume 1},
   :nemeses [#unprintable "jepsen.nemesis.combined$partition_nemesis$reify__16416@41cfcbb5"
             #unprintable "jepsen.nemesis.combined$db_nemesis$reify__16397@40941b54"]})
 :nodes ["n0"]
 :test-count 1
 :latency {:mean 0, :dist :constant}
 :bin "challange_3.py"
 :generator
 ((jepsen.generator.Synchronize
   {:gen (jepsen.generator.TimeLimit
          {:limit 20000000000,
           :cutoff nil,
           :gen (jepsen.generator.Any
                 {:gens [(jepsen.generator.OnThreads
                          {:f #{:nemesis},
                           :context-filter #object[jepsen.generator.context$make_thread_filter$lazy_filter__9167
                                                   "0xd15f98a"
                                                   "jepsen.generator.context$make_thread_filter$lazy_filter__9167@d15f98a"],
                           :gen nil})
                         (jepsen.generator.OnThreads
                          {:f #jepsen.generator.context.AllBut{:element :nemesis},
                           :context-filter #object[jepsen.generator.context$make_thread_filter$lazy_filter__9167
                                                   "0x704c3ca2"
                                                   "jepsen.generator.context$make_thread_filter$lazy_filter__9167@704c3ca2"],
                           :gen (jepsen.generator.Stagger
                                 {:dt 200000000,
                                  :next-time nil,
                                  :gen (jepsen.generator.Mix
                                        {:i 1,
                                         :gens [({:f :broadcast, :value 0}
                                                 {:f :broadcast, :value 1}
                                                 {:f :broadcast, :value 2}
                                                 {:f :broadcast, :value 3}
                                                 {:f :broadcast, :value 4}
                                                 {:f :broadcast, :value 5}
                                                 {:f :broadcast, :value 6}
                                                 {:f :broadcast, :value 7}
                                                 ...)
                                                ({:f :read}
                                                 {:f :read}
                                                 {:f :read}
                                                 {:f :read}
                                                 {:f :read}
                                                 {:f :read}
                                                 {:f :read}
                                                 {:f :read}
                                                 ...)]})})})]})})})
  (jepsen.generator.Synchronize
   {:gen (jepsen.generator.OnThreads
          {:f #{:nemesis},
           :context-filter #object[jepsen.generator.context$make_thread_filter$lazy_filter__9167
                                   "0x2a2f7a61"
                                   "jepsen.generator.context$make_thread_filter$lazy_filter__9167@2a2f7a61"],
           :gen ()})})
  (jepsen.generator.Synchronize
   {:gen {:type :log, :value "Waiting for recovery..."}})
  (jepsen.generator.Synchronize {:gen {:type :sleep, :value 10}})
  (jepsen.generator.Synchronize
   {:gen (jepsen.generator.OnThreads
          {:f #jepsen.generator.context.AllBut{:element :nemesis},
           :context-filter #object[jepsen.generator.context$make_thread_filter$lazy_filter__9167
                                   "0x8d40f07"
                                   "jepsen.generator.context$make_thread_filter$lazy_filter__9167@8d40f07"],
           :gen (jepsen.generator.EachThread
                 {:fresh-gen {:f :read, :final? true},
                  :context-filters #object[clojure.core$promise$reify__8591
                                           "0x196c8b93"
                                           {:status :pending, :val nil}],
                  :gens {}})})}))
 :log-net-recv false
 :os
 #object[maelstrom.net$jepsen_os$reify__15254
         "0x307ca947"
         "maelstrom.net$jepsen_os$reify__15254@307ca947"]
 :time-limit 20
 :workload :broadcast
 :consistency-models [:strict-serializable]
 :topology :grid}

INFO [2024-01-06 15:07:52,560] jepsen node n0 - maelstrom.net Starting Maelstrom network
INFO [2024-01-06 15:07:52,561] jepsen test runner - jepsen.db Tearing down DB
INFO [2024-01-06 15:07:52,562] jepsen test runner - jepsen.db Setting up DB
INFO [2024-01-06 15:07:52,562] jepsen node n0 - maelstrom.service Starting services: (lin-kv lin-tso lww-kv seq-kv)
INFO [2024-01-06 15:07:52,563] jepsen node n0 - maelstrom.db Setting up n0
INFO [2024-01-06 15:07:52,564] jepsen node n0 - maelstrom.process launching challange_3.py []
INFO [2024-01-06 15:07:52,655] jepsen test runner - jepsen.core Relative time begins now
INFO [2024-01-06 15:07:52,664] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:52,666] jepsen worker 0 - jepsen.util 0	:ok	:read	[]
INFO [2024-01-06 15:07:52,845] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	0
INFO [2024-01-06 15:07:52,847] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	0
INFO [2024-01-06 15:07:53,025] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:53,030] jepsen worker 0 - jepsen.util 0	:ok	:read	[0]
INFO [2024-01-06 15:07:53,072] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:53,074] jepsen worker 0 - jepsen.util 0	:ok	:read	[0]
INFO [2024-01-06 15:07:53,251] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	1
INFO [2024-01-06 15:07:53,254] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	1
INFO [2024-01-06 15:07:53,410] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:53,415] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1]
INFO [2024-01-06 15:07:53,490] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	2
INFO [2024-01-06 15:07:53,492] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	2
INFO [2024-01-06 15:07:53,513] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:53,517] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2]
INFO [2024-01-06 15:07:53,591] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:53,595] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2]
INFO [2024-01-06 15:07:53,708] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	3
INFO [2024-01-06 15:07:53,711] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	3
INFO [2024-01-06 15:07:53,872] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	4
INFO [2024-01-06 15:07:53,876] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	4
INFO [2024-01-06 15:07:53,962] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	5
INFO [2024-01-06 15:07:53,966] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	5
INFO [2024-01-06 15:07:53,977] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:53,979] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5]
INFO [2024-01-06 15:07:54,056] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	6
INFO [2024-01-06 15:07:54,070] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	6
INFO [2024-01-06 15:07:54,148] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	7
INFO [2024-01-06 15:07:54,155] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	7
INFO [2024-01-06 15:07:54,325] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	8
INFO [2024-01-06 15:07:54,330] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	8
INFO [2024-01-06 15:07:54,414] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	9
INFO [2024-01-06 15:07:54,417] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	9
INFO [2024-01-06 15:07:54,553] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:54,558] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9]
INFO [2024-01-06 15:07:54,706] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:54,711] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9]
INFO [2024-01-06 15:07:54,808] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:54,813] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9]
INFO [2024-01-06 15:07:54,886] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	10
INFO [2024-01-06 15:07:54,891] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	10
INFO [2024-01-06 15:07:55,006] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	11
INFO [2024-01-06 15:07:55,010] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	11
INFO [2024-01-06 15:07:55,174] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,178] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11]
INFO [2024-01-06 15:07:55,193] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,197] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11]
INFO [2024-01-06 15:07:55,372] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,377] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11]
INFO [2024-01-06 15:07:55,560] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	12
INFO [2024-01-06 15:07:55,562] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	12
INFO [2024-01-06 15:07:55,702] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,706] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12]
INFO [2024-01-06 15:07:55,770] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,773] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12]
INFO [2024-01-06 15:07:55,849] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	13
INFO [2024-01-06 15:07:55,854] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	13
INFO [2024-01-06 15:07:55,944] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	14
INFO [2024-01-06 15:07:55,948] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	14
INFO [2024-01-06 15:07:55,951] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,952] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14]
INFO [2024-01-06 15:07:55,980] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:55,984] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14]
INFO [2024-01-06 15:07:56,131] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	15
INFO [2024-01-06 15:07:56,135] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	15
INFO [2024-01-06 15:07:56,209] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:56,214] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15]
INFO [2024-01-06 15:07:56,247] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	16
INFO [2024-01-06 15:07:56,249] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	16
INFO [2024-01-06 15:07:56,282] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	17
INFO [2024-01-06 15:07:56,284] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	17
INFO [2024-01-06 15:07:56,486] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:56,488] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17]
INFO [2024-01-06 15:07:56,648] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	18
INFO [2024-01-06 15:07:56,652] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	18
INFO [2024-01-06 15:07:56,784] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:56,789] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18]
INFO [2024-01-06 15:07:56,848] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:56,850] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18]
INFO [2024-01-06 15:07:56,931] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	19
INFO [2024-01-06 15:07:56,934] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	19
INFO [2024-01-06 15:07:57,091] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:57,096] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19]
INFO [2024-01-06 15:07:57,262] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:57,266] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19]
INFO [2024-01-06 15:07:57,447] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:57,452] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19]
INFO [2024-01-06 15:07:57,576] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	20
INFO [2024-01-06 15:07:57,579] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	20
INFO [2024-01-06 15:07:57,642] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	21
INFO [2024-01-06 15:07:57,647] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	21
INFO [2024-01-06 15:07:57,776] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	22
INFO [2024-01-06 15:07:57,781] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	22
INFO [2024-01-06 15:07:57,841] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	23
INFO [2024-01-06 15:07:57,842] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	23
INFO [2024-01-06 15:07:57,882] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	24
INFO [2024-01-06 15:07:57,883] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	24
INFO [2024-01-06 15:07:58,048] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	25
INFO [2024-01-06 15:07:58,051] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	25
INFO [2024-01-06 15:07:58,229] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	26
INFO [2024-01-06 15:07:58,232] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	26
INFO [2024-01-06 15:07:58,257] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	27
INFO [2024-01-06 15:07:58,260] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	27
INFO [2024-01-06 15:07:58,397] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	28
INFO [2024-01-06 15:07:58,402] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	28
INFO [2024-01-06 15:07:58,449] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	29
INFO [2024-01-06 15:07:58,450] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	29
INFO [2024-01-06 15:07:58,551] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	30
INFO [2024-01-06 15:07:58,555] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	30
INFO [2024-01-06 15:07:58,570] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	31
INFO [2024-01-06 15:07:58,574] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	31
INFO [2024-01-06 15:07:58,582] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:58,585] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31]
INFO [2024-01-06 15:07:58,762] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	32
INFO [2024-01-06 15:07:58,765] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	32
INFO [2024-01-06 15:07:58,960] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	33
INFO [2024-01-06 15:07:58,964] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	33
INFO [2024-01-06 15:07:59,152] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	34
INFO [2024-01-06 15:07:59,156] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	34
INFO [2024-01-06 15:07:59,269] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	35
INFO [2024-01-06 15:07:59,272] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	35
INFO [2024-01-06 15:07:59,360] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	36
INFO [2024-01-06 15:07:59,366] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	36
INFO [2024-01-06 15:07:59,513] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:59,518] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36]
INFO [2024-01-06 15:07:59,530] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:59,533] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36]
INFO [2024-01-06 15:07:59,650] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	37
INFO [2024-01-06 15:07:59,654] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	37
INFO [2024-01-06 15:07:59,707] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:07:59,711] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37]
INFO [2024-01-06 15:07:59,847] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	38
INFO [2024-01-06 15:07:59,850] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	38
INFO [2024-01-06 15:07:59,869] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	39
INFO [2024-01-06 15:07:59,870] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	39
INFO [2024-01-06 15:08:00,038] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,042] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39]
INFO [2024-01-06 15:08:00,194] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,198] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39]
INFO [2024-01-06 15:08:00,281] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	40
INFO [2024-01-06 15:08:00,284] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	40
INFO [2024-01-06 15:08:00,316] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	41
INFO [2024-01-06 15:08:00,318] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	41
INFO [2024-01-06 15:08:00,383] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	42
INFO [2024-01-06 15:08:00,384] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	42
INFO [2024-01-06 15:08:00,387] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	43
INFO [2024-01-06 15:08:00,387] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	43
INFO [2024-01-06 15:08:00,475] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	44
INFO [2024-01-06 15:08:00,480] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	44
INFO [2024-01-06 15:08:00,495] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,501] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44]
INFO [2024-01-06 15:08:00,615] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,620] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44]
INFO [2024-01-06 15:08:00,623] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	45
INFO [2024-01-06 15:08:00,624] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	45
INFO [2024-01-06 15:08:00,755] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	46
INFO [2024-01-06 15:08:00,759] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	46
INFO [2024-01-06 15:08:00,849] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,855] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46]
INFO [2024-01-06 15:08:00,923] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,925] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46]
INFO [2024-01-06 15:08:00,940] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:00,941] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46]
INFO [2024-01-06 15:08:01,043] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:01,048] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46]
INFO [2024-01-06 15:08:01,132] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:01,137] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46]
INFO [2024-01-06 15:08:01,331] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	47
INFO [2024-01-06 15:08:01,335] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	47
INFO [2024-01-06 15:08:01,451] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	48
INFO [2024-01-06 15:08:01,454] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	48
INFO [2024-01-06 15:08:01,466] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	49
INFO [2024-01-06 15:08:01,469] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	49
INFO [2024-01-06 15:08:01,654] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	50
INFO [2024-01-06 15:08:01,656] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	50
INFO [2024-01-06 15:08:01,672] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	51
INFO [2024-01-06 15:08:01,674] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	51
INFO [2024-01-06 15:08:01,702] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	52
INFO [2024-01-06 15:08:01,703] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	52
INFO [2024-01-06 15:08:01,851] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	53
INFO [2024-01-06 15:08:01,853] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	53
INFO [2024-01-06 15:08:01,896] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:01,898] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53]
INFO [2024-01-06 15:08:02,102] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:02,106] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53]
INFO [2024-01-06 15:08:02,271] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:02,275] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53]
INFO [2024-01-06 15:08:02,454] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	54
INFO [2024-01-06 15:08:02,459] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	54
INFO [2024-01-06 15:08:02,605] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	55
INFO [2024-01-06 15:08:02,609] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	55
INFO [2024-01-06 15:08:02,677] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:02,682] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55]
INFO [2024-01-06 15:08:02,748] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:02,752] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55]
INFO [2024-01-06 15:08:02,805] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:02,807] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55]
INFO [2024-01-06 15:08:02,842] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	56
INFO [2024-01-06 15:08:02,845] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	56
INFO [2024-01-06 15:08:02,900] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:02,904] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56]
INFO [2024-01-06 15:08:03,059] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:03,064] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56]
INFO [2024-01-06 15:08:03,182] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:03,186] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56]
INFO [2024-01-06 15:08:03,384] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	57
INFO [2024-01-06 15:08:03,388] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	57
INFO [2024-01-06 15:08:03,497] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:03,501] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57]
INFO [2024-01-06 15:08:03,525] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	58
INFO [2024-01-06 15:08:03,532] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	58
INFO [2024-01-06 15:08:03,584] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:03,586] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58]
INFO [2024-01-06 15:08:03,733] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:03,739] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58]
INFO [2024-01-06 15:08:03,774] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:03,776] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58]
INFO [2024-01-06 15:08:03,968] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	59
INFO [2024-01-06 15:08:03,973] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	59
INFO [2024-01-06 15:08:04,141] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	60
INFO [2024-01-06 15:08:04,145] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	60
INFO [2024-01-06 15:08:04,280] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	61
INFO [2024-01-06 15:08:04,284] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	61
INFO [2024-01-06 15:08:04,296] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:04,297] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61]
INFO [2024-01-06 15:08:04,423] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	62
INFO [2024-01-06 15:08:04,426] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	62
INFO [2024-01-06 15:08:04,489] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	63
INFO [2024-01-06 15:08:04,492] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	63
INFO [2024-01-06 15:08:04,556] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:04,560] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63]
INFO [2024-01-06 15:08:04,643] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	64
INFO [2024-01-06 15:08:04,649] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	64
INFO [2024-01-06 15:08:04,692] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:04,694] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64]
INFO [2024-01-06 15:08:04,815] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	65
INFO [2024-01-06 15:08:04,819] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	65
INFO [2024-01-06 15:08:05,010] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,015] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65]
INFO [2024-01-06 15:08:05,039] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,042] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65]
INFO [2024-01-06 15:08:05,113] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	66
INFO [2024-01-06 15:08:05,118] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	66
INFO [2024-01-06 15:08:05,210] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,214] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66]
INFO [2024-01-06 15:08:05,215] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,216] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66]
INFO [2024-01-06 15:08:05,259] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	67
INFO [2024-01-06 15:08:05,261] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	67
INFO [2024-01-06 15:08:05,338] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	68
INFO [2024-01-06 15:08:05,342] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	68
INFO [2024-01-06 15:08:05,411] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	69
INFO [2024-01-06 15:08:05,422] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	69
INFO [2024-01-06 15:08:05,431] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	70
INFO [2024-01-06 15:08:05,432] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	70
INFO [2024-01-06 15:08:05,476] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,477] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70]
INFO [2024-01-06 15:08:05,650] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,655] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70]
INFO [2024-01-06 15:08:05,819] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:05,824] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70]
INFO [2024-01-06 15:08:05,895] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	71
INFO [2024-01-06 15:08:05,898] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	71
INFO [2024-01-06 15:08:05,976] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	72
INFO [2024-01-06 15:08:05,978] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	72
INFO [2024-01-06 15:08:06,105] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	73
INFO [2024-01-06 15:08:06,108] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	73
INFO [2024-01-06 15:08:06,309] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:06,313] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73]
INFO [2024-01-06 15:08:06,424] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	74
INFO [2024-01-06 15:08:06,427] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	74
INFO [2024-01-06 15:08:06,608] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	75
INFO [2024-01-06 15:08:06,611] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	75
INFO [2024-01-06 15:08:06,802] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:06,807] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75]
INFO [2024-01-06 15:08:06,977] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	76
INFO [2024-01-06 15:08:06,981] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	76
INFO [2024-01-06 15:08:07,139] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	77
INFO [2024-01-06 15:08:07,143] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	77
INFO [2024-01-06 15:08:07,258] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	78
INFO [2024-01-06 15:08:07,266] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	78
INFO [2024-01-06 15:08:07,413] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	79
INFO [2024-01-06 15:08:07,417] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	79
INFO [2024-01-06 15:08:07,474] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:07,477] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79]
INFO [2024-01-06 15:08:07,676] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:07,680] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79]
INFO [2024-01-06 15:08:07,784] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:07,788] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79]
INFO [2024-01-06 15:08:07,849] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:07,852] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79]
INFO [2024-01-06 15:08:07,924] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:07,928] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79]
INFO [2024-01-06 15:08:08,090] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:08,094] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79]
INFO [2024-01-06 15:08:08,264] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	80
INFO [2024-01-06 15:08:08,268] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	80
INFO [2024-01-06 15:08:08,451] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	81
INFO [2024-01-06 15:08:08,456] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	81
INFO [2024-01-06 15:08:08,542] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:08,543] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81]
INFO [2024-01-06 15:08:08,640] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	82
INFO [2024-01-06 15:08:08,642] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	82
INFO [2024-01-06 15:08:08,785] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:08,789] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82]
INFO [2024-01-06 15:08:08,818] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	83
INFO [2024-01-06 15:08:08,819] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	83
INFO [2024-01-06 15:08:08,852] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:08,854] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83]
INFO [2024-01-06 15:08:08,950] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:08,956] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83]
INFO [2024-01-06 15:08:09,113] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:09,117] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83]
INFO [2024-01-06 15:08:09,287] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:09,290] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83]
INFO [2024-01-06 15:08:09,359] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	84
INFO [2024-01-06 15:08:09,363] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	84
INFO [2024-01-06 15:08:09,376] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	85
INFO [2024-01-06 15:08:09,381] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	85
INFO [2024-01-06 15:08:09,425] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:09,430] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85]
INFO [2024-01-06 15:08:09,605] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	86
INFO [2024-01-06 15:08:09,608] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	86
INFO [2024-01-06 15:08:09,703] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:09,707] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86]
INFO [2024-01-06 15:08:09,777] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	87
INFO [2024-01-06 15:08:09,780] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	87
INFO [2024-01-06 15:08:09,891] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	88
INFO [2024-01-06 15:08:09,896] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	88
INFO [2024-01-06 15:08:09,999] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,004] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88]
INFO [2024-01-06 15:08:10,023] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,026] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88]
INFO [2024-01-06 15:08:10,218] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	89
INFO [2024-01-06 15:08:10,222] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	89
INFO [2024-01-06 15:08:10,359] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,363] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89]
INFO [2024-01-06 15:08:10,405] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	90
INFO [2024-01-06 15:08:10,406] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	90
INFO [2024-01-06 15:08:10,497] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,501] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90]
INFO [2024-01-06 15:08:10,606] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,611] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90]
INFO [2024-01-06 15:08:10,710] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	91
INFO [2024-01-06 15:08:10,715] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	91
INFO [2024-01-06 15:08:10,824] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,828] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91]
INFO [2024-01-06 15:08:10,850] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:10,854] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91]
INFO [2024-01-06 15:08:11,055] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	92
INFO [2024-01-06 15:08:11,057] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	92
INFO [2024-01-06 15:08:11,183] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:11,187] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92]
INFO [2024-01-06 15:08:11,225] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	93
INFO [2024-01-06 15:08:11,226] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	93
INFO [2024-01-06 15:08:11,374] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	94
INFO [2024-01-06 15:08:11,377] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	94
INFO [2024-01-06 15:08:11,456] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	95
INFO [2024-01-06 15:08:11,459] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	95
INFO [2024-01-06 15:08:11,545] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	96
INFO [2024-01-06 15:08:11,548] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	96
INFO [2024-01-06 15:08:11,608] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	97
INFO [2024-01-06 15:08:11,609] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	97
INFO [2024-01-06 15:08:11,682] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:11,685] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97]
INFO [2024-01-06 15:08:11,789] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:11,793] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97]
INFO [2024-01-06 15:08:11,981] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:11,984] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97]
INFO [2024-01-06 15:08:12,149] jepsen worker 0 - jepsen.util 0	:invoke	:broadcast	98
INFO [2024-01-06 15:08:12,154] jepsen worker 0 - jepsen.util 0	:ok	:broadcast	98
INFO [2024-01-06 15:08:12,287] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:12,292] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97 98]
INFO [2024-01-06 15:08:12,378] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:12,379] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97 98]
INFO [2024-01-06 15:08:12,512] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:12,519] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97 98]
INFO [2024-01-06 15:08:12,519] jepsen worker nemesis - jepsen.generator.interpreter Waiting for recovery...
INFO [2024-01-06 15:08:22,530] jepsen worker 0 - jepsen.util 0	:invoke	:read	nil
INFO [2024-01-06 15:08:22,533] jepsen worker 0 - jepsen.util 0	:ok	:read	[0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 51 52 53 54 55 56 57 58 59 60 61 62 63 64 65 66 67 68 69 70 71 72 73 74 75 76 77 78 79 80 81 82 83 84 85 86 87 88 89 90 91 92 93 94 95 96 97 98]
INFO [2024-01-06 15:08:22,552] jepsen test runner - jepsen.core Run complete, writing
INFO [2024-01-06 15:08:22,610] jepsen node n0 - maelstrom.db Tearing down n0
INFO [2024-01-06 15:08:23,690] jepsen node n0 - maelstrom.net Shutting down Maelstrom network
INFO [2024-01-06 15:08:23,693] jepsen test runner - jepsen.core Analyzing...
INFO [2024-01-06 15:08:23,921] jepsen test runner - jepsen.core Analysis complete
INFO [2024-01-06 15:08:23,928] jepsen results - jepsen.store Wrote /Users/pankaj.negi/Desktop/repos/maelstrom-problems/store/broadcast/20240106T150751.664+0530/results.edn
INFO [2024-01-06 15:08:23,946] jepsen test runner - jepsen.core {:perf {:latency-graph {:valid? true},
        :rate-graph {:valid? true},
        :valid? true},
 :timeline {:valid? true},
 :exceptions {:valid? true},
 :stats {:valid? true,
         :count 190,
         :ok-count 190,
         :fail-count 0,
         :info-count 0,
         :by-f {:broadcast {:valid? true,
                            :count 99,
                            :ok-count 99,
                            :fail-count 0,
                            :info-count 0},
                :read {:valid? true,
                       :count 91,
                       :ok-count 91,
                       :fail-count 0,
                       :info-count 0}}},
 :availability {:valid? true, :ok-fraction 1.0},
 :net {:all {:send-count 384,
             :recv-count 384,
             :msg-count 384,
             :msgs-per-op 2.0210526},
       :clients {:send-count 384, :recv-count 384, :msg-count 384},
       :servers {:send-count 0,
                 :recv-count 0,
                 :msg-count 0,
                 :msgs-per-op 0.0},
       :valid? true},
 :workload {:worst-stale (),
            :duplicated-count 0,
            :valid? true,
            :lost-count 0,
            :lost (),
            :stable-count 99,
            :stale-count 0,
            :stale (),
            :never-read-count 0,
            :stable-latencies {0 0, 0.5 0, 0.95 0, 0.99 0, 1 0},
            :attempt-count 99,
            :never-read (),
            :duplicated {}},
 :valid? true}


Everything looks good! ヽ(‘ー`)ノ
```