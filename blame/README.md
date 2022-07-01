`git blame` is a really useful command: When you collaborate in a team project using `git` as version control and
when you want to inspect who wrote a particular line in a particular file, you simple `git blame <that_file>` and
you will get a pager, which details each line's

- commit id
- author
- datetime of birth

For example, the following is the first 14 lines of the file `coroutines.py` of `asyncio` in
CPython's github source code:
```
a1092f62492 (Illia Volochii   2021-07-01 16:13:59 +0300   1) __all__ = 'iscoroutinefunction', 'iscoroutine'
f951d28ac89 (Victor Stinner   2014-06-29 00:46:45 +0200   2)
a9d7e552c72 (Yury Selivanov   2017-12-19 07:18:45 -0500   3) import collections.abc
f951d28ac89 (Victor Stinner   2014-06-29 00:46:45 +0200   4) import inspect
f951d28ac89 (Victor Stinner   2014-06-29 00:46:45 +0200   5) import os
f951d28ac89 (Victor Stinner   2014-06-29 00:46:45 +0200   6) import sys
f951d28ac89 (Victor Stinner   2014-06-29 00:46:45 +0200   7) import traceback
b75380f3336 (Victor Stinner   2014-06-30 14:39:11 +0200   8) import types
f951d28ac89 (Victor Stinner   2014-06-29 00:46:45 +0200   9)
b75380f3336 (Victor Stinner   2014-06-30 14:39:11 +0200  10)
44862df2eee (Victor Stinner   2017-11-20 07:14:07 -0800  11) def _is_debug_mode():
a1092f62492 (Illia Volochii   2021-07-01 16:13:59 +0300  12)     # See: https://docs.python.org/3/library/asyncio-dev.html#asyncio-debug-mode.
6370f345e1d (Yury Selivanov   2017-12-10 18:36:12 -0500  13)     return sys.flags.dev_mode or (not sys.flags.ignore_environment and
6370f345e1d (Yury Selivanov   2017-12-10 18:36:12 -0500  14)                                   bool(os.environ.get('PYTHONASYNCIODEBUG')))
```
