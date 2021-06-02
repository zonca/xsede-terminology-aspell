# XSEDE inclusive terminology spell checking with aspell

English spellchecking with `aspell` which suggests replacement for non-inclusive terms.
It currently just includes 1 word from the XSEDE terminology list.

See <https://www.xsede.org/terminology>

## Usage

All options are passed to `aspell`:

    bash spellcheck.sh sample_text.txt
    bash spellcheck.sh -t your_own_text.tex
    bash spellcheck.sh -M your_own_text.md

`sample_text.txt` is included in the repository for testing purposes.

## How to add more words

* Remove all the forms of the non-inclusive word from `en_xsede_terminology.wordlist` (see [b6aaecb1d413](https://github.com/zonca/xsede-terminology-aspell/commit/b6aaecb1d4137ba98268b43785af2cfa01d26ff0))
* Build the dictionary with: `bash create_dictionary.sh`
* Add the replacements to `xsede-terminology.en.prepl`, see existing words as an example

## Example

I added ** to show the word highlighted by the interactive spellchecker.

```
> bash spellcheck.sh sample_text.txt
Standard word spelled incorrectly: **computr**
Not inclusive term spelled correctly: abort
Not inclusive term spelled correctly: aborted
Not inclusive term spelled incorrectly: abbort

                                                                                                                   
1) compute                                               6) comport
2) computer                                              7) compete
3) computed                                              8) compote
4) computers                                             9) computer's
5) computes
i) Ignore                                                I) Ignore all
r) Replace                                               R) Replace all
a) Add                                                   l) Add Lower
b) Abort                                                 x) Exit
                                                                                                                   
? 
```

```
Standard word spelled incorrectly: computr
Not inclusive term spelled correctly: **abort**
Not inclusive term spelled correctly: aborted
Not inclusive term spelled incorrectly: abbort
                                                                                                                   
1) cancel                                                6) abet
2) end                                                   7) cancellations
3) about                                                 8) endings
4) Abbott                                                9) aboard
5) abbot                                                 0) abut
i) Ignore                                                I) Ignore all
r) Replace                                               R) Replace all
a) Add                                                   l) Add Lower
b) Abort                                                 x) Exit
```

```
Standard word spelled incorrectly: computr
Not inclusive term spelled correctly: abort
Not inclusive term spelled correctly: **aborted**
Not inclusive term spelled incorrectly: abbort
                                                                                                                   
1) canceled                                              6) cancellations
2) ended                                                 7) endings
3) abetted                                               8) cancel 
4) abutted                                               9) end
5) abated                                                0) assorted
i) Ignore                                                I) Ignore all
r) Replace                                               R) Replace all
a) Add                                                   l) Add Lower
b) Abort                                                 x) Exit
```

```
Standard word spelled incorrectly: computr
Not inclusive term spelled correctly: abort
Not inclusive term spelled correctly: aborted
Not inclusive term spelled incorrectly: **abbort**
                                                                                                                   
1) Abbott                                                4) end
2) abbot                                                 5) about  
3) cancel


i) Ignore                                                I) Ignore all
r) Replace                                               R) Replace all
a) Add                                                   l) Add Lower
b) Abort                                                 x) Exit
```
