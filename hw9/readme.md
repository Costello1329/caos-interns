### HW 9.1: Ping pong, pt.1

You need to create two programs: `ping.c` and `pong.c`. On startup, **pong** should print its pid and **ping** - should receive **pong**'s pid as argument (via argv).
On startup, **ping** should send a `SIGUSR1` signal to **pong** and print `ping`. **Pong** should print `pong` after receiving the `SIGUSR1` signal.


#### Example
Compile: `gcc ping.c -o ping && gcc pong.c -o pong` \
Run **Pong**: `./pong` \
**Pong** outputs its pid: `23942` \
Run **Ping** (in the different terminal): `./ping 23942` \
**Ping** prints out: `ping` \
**Pong** prints out: `pong`

#### Deadline:
Apr 5, 23:59:59

#### Points:
This task costs 6pts


### HW 9.2: Ping pong, pt.2

You need to create two programs: `ping.c` and `pong.c`. On startup, both **ping** and **pong** should print therirs pid and **ping** - should receive **pong**'s pid as argument (via argv).
On startup, **ping** should receive the value from the stdin and send a `SIGRTMIN` signal to a **pong** (pid has been provided through the argument) and print `ping %d`, where `%d` is a value that it read. **Pong** should print `pong %d`, where `%d` is a value that it received via `SIGRTMIN` signal. Then, **pong** should send the signal back to the **ping** with the value increased by 1. Then, **ping** should send the signal to **pong** with the same value, etc... Also, **ping** should properly handle `SIGTERM`: it should send `SIGTERM` to **pong** and die **right after** that!

#### Important
You should add delays between receiving the signal and sending it back. Otherwise, program won't work properly. You can add **1s** delay with function `sleep(1)` which is defined in `unistd.h`

#### Example
Compile: `gcc ping.c -o ping && gcc pong.c -o pong` \
Run **Pong**: `./pong` \
**Pong** outputs its pid: `23942` \
Run **Ping** (in the different terminal): `./ping 23942` \
**Ping** outputs its pid: `23943` \
**Ping** prints out: `Enter the value to pong: `, user writes `5`
**Ping** prints out: `ping 5` \
**Pong** prints out: `pong 5` \
**Ping** prints out: `ping 6` \
**Pong** prints out: `pong 6` \
**Ping** prints out: `ping 7` \
**Pong** prints out: `pong 7` \
**Ping** prints out: `ping 8` \
**Pong** prints out: `pong 8` \
User is tired now, so he send `SIGTERM` to **ping**: `kill -SIGTERM 23943`

#### Deadline:
Apr 12, 23:59:59

#### Points:
This task costs 8pts
