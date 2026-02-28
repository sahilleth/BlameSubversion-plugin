# BlameSubversion Plugin

This plug-in provides utilities for getting svn info from upstream job to downstream job.

The original purpose of creating BlameSubversion is to solve [JENKINS-7509](https://issues.jenkins.io/browse/JENKINS-7509).

**Why need BlameSubversion plugin?**

![](docs/images/why_need_BlameSubversion.jpg)

*When somebody checks in the code, the Upstream job1 or upstream job2 will build the source code.
*When the upstream job1 or upstream job2 is done, it will invoke the build of downstream job2.
*When the downstream job2 build failed, the svn info about who checked in upstream job1 or upstream job2 was lost.

**How did BlameSubversion plugin work?**

*1 get the build of upstream job who trigger this build of downstream
*2 get svn info from it
*3 copy svn info to downstream build
*4 provide interfaces for other official hudson plugins.

**Easy configure of BlameSubversion plugin**

1. Choose the checkbox of Blame Subversion in Source code Management
2. Choose the checkbox of Always Collect SVN info from upstream job if you are sure to do it.

## Changelog

##### Version 1.200 (Jan 4, 2012)

- Release 1.200 to get rid of version order issue with 1.121 (assuming this was a typo releasing 1.21)

##### Version 1.25 (Nov 1, 2010)

- Fix a bug

##### Version 1.24 (Nov 1, 2010)

- Add new feature for up down stream job build number synchronize
- Add help.html
- Fix a bug for notify

##### Version 1.121 (Oct 15, 2010)
