### HW 9.1: Ping pong, pt.1

You need to create two programs: `ping.c` and `pong.c`. On startup, **pong** should print its pid and **ping** - should receive **pong**'s pid as argument (via argv).
On startup, **ping** should send a `SIGUSR1` signal to **pong** and print `ping`. **Pong** should print `pong` after receiving the `SIGUSR1` signal.


#### Example
Compile: `gcc ping.c -o ping && gcc pong.c -o pong` \
Run **pong**: `./pong` \
**Pong** outputs its pid: `23942` \
Run **ping**: `./ping 23942` \
**Ping** prints out: `ping` \
**Pong** prints out: `pong`

#### Deadline:
Apr 5, 23:59:59

#### Points:
This task costs 6pts
