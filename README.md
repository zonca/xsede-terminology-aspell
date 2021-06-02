# XSEDE inclusive terminology spell checking with aspell

See https://www.xsede.org/terminology

## Example

I added ** to show the word highlighted by the interactive spellchecker.

```
> bash spellcheck.sh
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
