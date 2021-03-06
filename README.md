vital-System-Job
==============================================================================
[![Travis CI](https://img.shields.io/travis/lambdalisue/vital-System-Job/master.svg?style=flat-square&label=Travis%20CI)](https://travis-ci.org/lambdalisue/vital-System-Job)
[![AppVeyor](https://img.shields.io/appveyor/ci/lambdalisue/vital-System-Job/master.svg?style=flat-square&label=AppVeyor)](https://ci.appveyor.com/project/lambdalisue/vital-System-Job/branch/master)
![Version 0.1.0-dev](https://img.shields.io/badge/version-0.1.0--dev-yellow.svg?style=flat-square)
![Support Vim 8.0.0027 or above](https://img.shields.io/badge/support-Vim%208.0.0027%20or%20above-yellowgreen.svg?style=flat-square)
![Support Neovim 0.1.7 or above](https://img.shields.io/badge/support-Neovim%200.1.7%20or%20above-yellowgreen.svg?style=flat-square)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square)](LICENSE.md)
[![Doc](https://img.shields.io/badge/doc-%3Ah%20System.Job-orange.svg?style=flat-square)](doc/Vital/System/Job.txt)
[![Doc](https://img.shields.io/badge/doc-%3Ah%20System.Process.Job-orange.svg?style=flat-square)](doc/Vital/System/Process/Job.txt)

This repository contains the following two Vital modules

- `System.Job` -- A job wrapper of Vim 8 and Neovim
- `System.Process.Job` -- A process client using `System.Job` internally


Usage
-------------------------------------------------------------------------------

Install the repository in your `runtimepath` and then

```vim
:Vitalize . +System.Job
:Vitalize . +System.Process.Job
```

Then

```vim
" System.Job
let s:Job = vital#vital#import('System.Job')
let job = s:Job.start(['git', 'status'])

" System.Process.Job
let s:Process = vital#vital#import('System.Process')
call s:Process.register('System.Process.Job')
let options = {
        \ 'clients': ['System.Process.Job'],
        \}
let result = s:Process.execute(['git', 'status'], options)
```
