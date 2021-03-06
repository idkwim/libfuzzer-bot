This page describes an [experimental fuzzer bot](http://104.197.61.218/) for [PCRE2](http://pcre.org).

The bot uses [libFuzzer](http://llvm.org/docs/LibFuzzer.html) and
[AddressSanitizer](http://clang.llvm.org/docs/AddressSanitizer.html) to find existing
bugs in PCRE2 and possible new regressions. Currently, the [target
function](./pcre_fuzzer.cc) is *very* simple, we'll be extending it in future.

The test corpus is 100% synthesised from scratch.

Bugs found by this bot and the preceeding manual process:
* Seach for `libFuzzer` in
  [bugzilla](https://bugs.exim.org/buglist.cgi?bug_status=__all__&content=libfuzzer&list_id=507&order=Importance&product=PCRE&query_format=specific).
* Search for `LLVM fuzzer` in the [ChangeLog](
  http://vcs.pcre.org/pcre2/code/trunk/ChangeLog?view=markup)

