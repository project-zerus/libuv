cc_library(
  name = 'libuv',
  incs = [
    'include',
    'include/uv-private',
    'src/',
  ],
  export_incs = [
    'include',
  ],
  defs = [
    '_GNU_SOURCE',
  ],
  extra_cppflags = [
    '--std=gnu89',
    '-Wall',
    '-Wextra',
    '-Wno-unused-parameter',
    '-Wstrict-aliasing',
  ],
  srcs = [
    'src/fs-poll.c',
    'src/inet.c',
    'src/uv-common.c',
    'src/version.c',
    'src/unix/async.c',
    'src/unix/core.c',
    'src/unix/dl.c',
    'src/unix/error.c',
    'src/unix/fs.c',
    'src/unix/getaddrinfo.c',
    'src/unix/loop.c',
    'src/unix/loop-watcher.c',
    'src/unix/pipe.c',
    'src/unix/poll.c',
    'src/unix/process.c',
    'src/unix/signal.c',
    'src/unix/stream.c',
    'src/unix/tcp.c',
    'src/unix/thread.c',
    'src/unix/threadpool.c',
    'src/unix/timer.c',
    'src/unix/tty.c',
    'src/unix/udp.c',
    'src/unix/proctitle.c',
    'src/unix/linux-core.c',
    'src/unix/linux-inotify.c',
    'src/unix/linux-syscalls.c',
  ],
  deps = [
    '#dl',
    '#rt',
    '#pthread',
  ]
)

cc_test(
  name = 'run-tests',
  warning = 'no',
  incs = [
    'include',
    'include/uv-private',
    'src/',
  ],
  defs = [
    '_GNU_SOURCE',
  ],
  extra_cppflags = [
    '--std=gnu89',
  ],
  testdata = [
    'test'
  ],
  srcs = [
    'test/blackhole-server.c',
    'test/echo-server.c',
    'test/run-tests.c',
    'test/runner.c',
    'test/test-get-loadavg.c',
    'test/test-util.c',
    'test/test-active.c',
    'test/test-async.c',
    'test/test-callback-stack.c',
    'test/test-callback-order.c',
    'test/test-connection-fail.c',
    'test/test-cwd-and-chdir.c',
    'test/test-delayed-accept.c',
    'test/test-error.c',
    'test/test-embed.c',
    'test/test-emfile.c',
    'test/test-fail-always.c',
    'test/test-fs.c',
    'test/test-fs-event.c',
    'test/test-get-currentexe.c',
    'test/test-get-memory.c',
    'test/test-getaddrinfo.c',
    'test/test-getsockname.c',
    'test/test-hrtime.c',
    'test/test-idle.c',
    'test/test-ipc.c',
    'test/test-ipc-send-recv.c',
    'test/test-loop-handles.c',
    'test/test-loop-stop.c',
    'test/test-walk-handles.c',
    'test/test-watcher-cross-stop.c',
    'test/test-multiple-listen.c',
    'test/test-osx-select.c',
    'test/test-pass-always.c',
    'test/test-ping-pong.c',
    'test/test-pipe-bind-error.c',
    'test/test-pipe-connect-error.c',
    'test/test-pipe-server-close.c',
    'test/test-platform-output.c',
    'test/test-poll.c',
    'test/test-poll-close.c',
    'test/test-poll-closesocket.c',
    'test/test-process-title.c',
    'test/test-ref.c',
    'test/test-run-nowait.c',
    'test/test-run-once.c',
    'test/test-semaphore.c',
    'test/test-shutdown-close.c',
    'test/test-shutdown-eof.c',
    'test/test-shutdown-twice.c',
    'test/test-signal.c',
    'test/test-signal-multiple-loops.c',
    'test/test-spawn.c',
    'test/test-fs-poll.c',
    'test/test-stdio-over-pipes.c',
    'test/test-tcp-bind-error.c',
    'test/test-tcp-bind6-error.c',
    'test/test-tcp-close.c',
    'test/test-tcp-close-accept.c',
    'test/test-tcp-close-while-connecting.c',
    'test/test-tcp-connect-error-after-write.c',
    'test/test-tcp-shutdown-after-write.c',
    'test/test-tcp-flags.c',
    'test/test-tcp-connect-error.c',
    'test/test-tcp-connect-timeout.c',
    'test/test-tcp-connect6-error.c',
    'test/test-tcp-open.c',
    'test/test-tcp-write-to-half-open-connection.c',
    'test/test-tcp-writealot.c',
    'test/test-tcp-unexpected-read.c',
    'test/test-tcp-read-stop.c',
    'test/test-threadpool.c',
    'test/test-threadpool-cancel.c',
    'test/test-mutexes.c',
    'test/test-thread.c',
    'test/test-barrier.c',
    'test/test-condvar.c',
    'test/test-timer-again.c',
    'test/test-timer-from-check.c',
    'test/test-timer.c',
    'test/test-tty.c',
    'test/test-udp-dgram-too-big.c',
    'test/test-udp-ipv6.c',
    'test/test-udp-open.c',
    'test/test-udp-options.c',
    'test/test-udp-send-and-recv.c',
    'test/test-udp-multicast-join.c',
    'test/test-dlerror.c',
    'test/test-udp-multicast-ttl.c',
    'test/runner-unix.c',
  ],
  deps = ':libuv'
)

cc_binary(
  name = 'run-benchmarks',
  warning = 'no',
  incs = [
    'include',
    'include/uv-private',
    'src/',
  ],
  defs = [
    '_GNU_SOURCE',
  ],
  extra_cppflags = [
    '--std=gnu89',
  ],
  srcs = [
    'test/benchmark-async.c',
    'test/benchmark-async-pummel.c',
    'test/benchmark-fs-stat.c',
    'test/benchmark-getaddrinfo.c',
    'test/benchmark-loop-count.c',
    'test/benchmark-million-async.c',
    'test/benchmark-million-timers.c',
    'test/benchmark-multi-accept.c',
    'test/benchmark-ping-pongs.c',
    'test/benchmark-pound.c',
    'test/benchmark-pump.c',
    'test/benchmark-sizes.c',
    'test/benchmark-spawn.c',
    'test/benchmark-thread.c',
    'test/benchmark-tcp-write-batch.c',
    'test/benchmark-udp-pummel.c',
    'test/dns-server.c',
    'test/echo-server.c',
    'test/blackhole-server.c',
    'test/run-benchmarks.c',
    'test/runner.c',
    'test/runner-unix.c',
  ],
  deps = ':libuv'
)
