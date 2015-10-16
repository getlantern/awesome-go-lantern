# Awesome Go for Lantern

Cool libraries, frameworks, tips and tricks and anything that can be useful to share.

Inspired by [awesome-go](https://github.com/avelino/awesome-go), for Lantern.



## General

*General tools, hacks and techniques with wide usage*

* [Preeny](https://github.com/zardus/preeny) - Make it easier to interact with services locally. It can disable fork(), rand(), and alarm() and can convert a server application to a console one.
* [Ratelimit](https://github.com/bsm/ratelimit) - Simple, thread-safe Go rate-limiter.


## Networking

* [Gopacket](https://github.com/google/gopacket) - Provides packet processing capabilities for Go.


## Network Analysis Tools

*Tools for interference detection, probing and network analysis in general*

* [Netalyzr](http://n1.netalyzr.icsi.berkeley.edu/analysis/)
* [OONI](https://github.com/TheTorProject/ooni-probe)
* [Zmap](https://zmap.io/)
* [NDT](http://www.measurementlab.net/tools/ndt)


## Testing

*Testing utilities and libraries*

* [Go-fuzz](https://github.com/dvyukov/go-fuzz) - Randomized testing (fuzzing). Mainly applicable to packages that parse complex inputs (both text and binary).
* [Stress](https://godoc.org/golang.org/x/tools/cmd/stress) - The stress utility is intended for catching of episodic failures. It runs a given process in parallel in a loop and collects any failures.


### Network-specific testing

*Libraries for network testing.*

* [Linkio](https://github.com/ian-kent/linkio) - Network link speed simulation for Reader/Writer interfaces.
* [Toxiproxy](https://github.com/shopify/toxiproxy) - Proxy to simulate network and system conditions for automated tests.
* [Comcast](https://github.com/tylertreat/Comcast) - Simulation of bad network connections.
* [Gor](https://github.com/buger/gor) - HTTP traffic replay in real-time. Replay traffic from production to staging and dev environments. Test code on real user sessions in an automated and repeatable fashion.


## Code Checking

*Tools for checking code style and related*

* [Errcheck](https://github.com/kisielk/errcheck) - Checking for unchecked errors in go programs.
* [Golint](https://github.com/golang/lint) - A linter for Go source code.


## Code Analysis

*Static code analysis tools that will help you gain insight of the codebase*

* [Oracle](https://godoc.org/golang.org/x/tools/cmd/oracle) - The go oracle is a source analysis tool that answers questions about Go programs.


## Code Refactoring

*Refactoring tools specific for Go*

* [Gorename](https://godoc.org/golang.org/x/tools/cmd/gorename) - Precise type-safe renaming of identifiers in Go source code.
* [Gomvpkg](https://godoc.org/golang.org/x/tools/cmd/gomvpkg) - Move go packages, updating import declarations.
* [Goimports](https://godoc.org/golang.org/x/tools/cmd/goimports) - Update Go import lines, adding missing ones and removing unreferenced ones.
* [Eg](https://godoc.org/golang.org/x/tools/refactor/) - Example-based refactoring tool (better instructions running it).


## Dynamic Analysis Tools

*Tools to inspect and study the program behavior at runtime*

* Race detection - ```go test -race```
* GC tracing - ```GODEBUG=gctrace=1 go run <file.go>```
* Scheduler tracing [(info)](http://www.goinggo.net/2015/02/scheduler-tracing-in-go.html) - ```GODEBUG=schedtrace=1000 go run <file.go>```
* Generic tracing [(info)](https://docs.google.com/document/u/1/d/1FP5apqzBgr7ahCCgFO-yoVhk4YZrNIDNf9RybngBc14/pub) - The capability is compiled into all programs always, and is enabled on demand -- when tracing is disabled it has minimal runtime overhead. That is, the trace can be obtained from a server in production serving live traffic. For visualization, use Google's [trace viewer](https://github.com/google/trace-viewer), or type the URL ```chrome://tracing``` for an embedded UI in Chrome.
* [panicparse](https://github.com/maruel/panicparse) - Groups similar goroutines and colorizes stack dump.
