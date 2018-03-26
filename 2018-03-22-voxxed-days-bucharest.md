Links:

* https://voxxeddays.com/romania/bucharest/2018-03-22/

day1 
-----
-----

netflix oss
--------------

github.com/mkheck

* spring cloud xonfig
* nerflix eureka
* netflix hystrix
* netflix ribbon
* netflix zuul/spring cloud gateway
* spring cloud stream
* spring cloud sleuth
* spring cloud security

kubernetes
--------------

* redhat openshift
* mini shift
* start kubernetes locally on your machine
* separate projs for stage/ci/prod
* blue/green deployment

   * caveats : long running sessions and db migrations
   * edson yanaga book about data migration in microservices
* manual promotion to prod from jenkins
* canary releases: only a small portion goes to new api

devops - advanced pipelines
---------------------------

* zuul - programmatic routing through groovy filters
* feature toggles - ff4j
* service mesh - istio, envoy (sidecart impl), mirroring - allows forwarding request through one prod api but also a new api
(to test perf, etc) , diffy allows to analyze returned results to see if there are differences
* Book : Migrating to microservice databases

react , state, graph ql
--------

* sizzy.io
* egghead.io redux lib tuorial by the auth
* dan abramov
* MobX alt to Redux
* ex tech choices for react: apollo, router, setState, form lib
* Apollo - listen for APPOLO_MUTATION_ERROR use redux-offline
* Next.js 
* break spa in miniapps by routes
* @thekitze

java Fn 
-------

* FaaS 
* we could have called it jeff - presentation
* composable function flows

day 2 voxxed
------------------
------------------

docker keynote
-------

* presentation - dockerizing aurea, bad neighbours - oss proj for docker constraints
* Container D - oss golang proj ti debug docker containers
* docker slow startup times - pprof, iptables to blame - patched dcker network component to make less iptables calls
* aws ELB kubernetes issues - long connection issues
* prefer recovery to fixing

flying services keynote
-----------------------------

* "everybody wants to get high"
* Poland, they use drones to map roads for self-driving cars
* yadrone frmwk control drone through software
* gps, ibeacon, computer vision - yaw
* edge based distance
* Probabilistic robotics
* particle filtering
* @kriskudrynski

istio
--------

* kubernetes - LB out of the box
* restart failing containers out of the box

iot microprofile
--------------------

* microprofile toolbox for microservices
* jee for iot

legacy projs
---------------

0) simplify onboarding

1) wrap it with e2e tests

2) split in modules, cut vertically, not horizontally

3) distillation

* singleton putrefaction : remove singleton hidden deps, use instances, use appcontext patterns
* use lambdas to reduce deps between classes
* @ramtop

class reloading
--------------------

* jdb for simple operations, redefine
* paper: "safe class and data evolution in long-lived java apps"
* "dynamic code evolution for java" 

spring into kotlin
--------------

* mark heckler

elasticsearch to legacy apps
--------------------

* aggregates
* fuzziness
* github.com/dadoonet/legacy-search

cqrs and event sourcing
-----------

* events are more important than data model in distributed systems
* cqs
* "asking a question should not change the answer"
* separate methods for read/write

	ex java : separate read/write java interfaces
* cqrs
* distributed data - sync techniques for write/reads
* transactions - write model
* entity - read model
* useful for analytics
* read datastores should have just views with necessary data to read, not entire entities
* reqs: latency, size, staleness, ownership, security, type
* in-memory data grids , index your queries instead of data - continuous queries - we only move data that changes through the network
* infinispan
* teiid.jboss.org - data virtualization eases separation of monolithic data
* msg brokers : active mq, kafka (persistence, order guarantee on same partition)
* vertx.io - use as proxy for an http endpoint - reactive gateway , vertx event bus
* change data capture - debezium.io


