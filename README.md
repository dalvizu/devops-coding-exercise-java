# DevOps coding exercise

This is a take-home programming assignment as part of the the interview
process. This consists of a coding problem and a two-part DevOps problem.
The purpose is to use your solution as a discussion topic with your potential
colleagues, to help understand how you think and approach a problem, in an
environment you'd expect to have on the job.

This whole problem is intended to anywhere between 2 to 16 hours, and we typically
encourage this to be done over a weekend, though you can take whatever time you need.

## Coding Problem:

As DevOps engineer, you are building the pipeline out to production. Your company's support
Support group has asked to be notified when a pipeline starts, and wants to
have its JIRA issue tracking system updated.

When the Pipeline starts, you'll have access to a set of git commits,
containing a commit message, sha, authorship. An example git commit:

```
commit 55c0bb88b6e4f096574991dd9217bcf8c745d05e
Author: Example User <example@example.com>
Date:   Thu Aug 4 17:09:19 2022 -0600

    SSD-101 super duper feature
    Fix tomcat issue with using forks over spoons.
```

These git commits will be provided as a `GitCommit` object by another program.

Your assignment is to write a method which returns the "issue key" in this commit: `SSD-101`,
and a general solution to return all of the issue keys present in any git commits provided.

Basically, implement this function: [App#get_jira_tickets()](https://github.com/dalvizu/devops-coding-exercise-java/blob/master/src/main/java/com/example/App.java#L15)

_Note_: The string 'SSD-101' is the 'key' of a JIRA issue. JIRA is a popular ticketing system in
software development and common in the open source community. The key of an issue is its project
name (`SSD`) followed by a hyphen and then a number (`101`). For more information on what an issue
is, see [what is an issue?](https://confluence.atlassian.com/jira064/what-is-an-issue-720416138.html)

If you have any questions, feel free to ask through your interviewer. You'll be asked to present your
solution to an interview panel of engineers and present your solution, so be prepared
to discuss your solution. Remember to document any assumptions you may be making.

## DevOps problem

### Docker problem

Containerize your solution in a Docker container. The container should be able to run both your
tests and the main application by running different commands

* create a `Dockerfile`
* provide instructions for how to build and run it.

### AWS problem

You have been provided an AWS IAM credential and a region to use in AWS. Please do not leave this region,
as we need clean up resources after the interview is done.

The problem is to take to take the java code and place an archive of it in a public website.
Create this website, registered under a domain name of your choosing, using the most appropriate technology
you can think of.

This website must include a zipped archive of your repo with any instructions you wish to provide about how
to use or evaluate your submission.

Please ensure this is not searchable by a search engine.

Note your website is not required to run any python code or have any sort of API. We just want to
see how you work with AWS, how you'd build a website with AWS, and how you'd hand off a completed
project for others to read and use.

Fancy HTML not required.

An infrastructure as code solution is required, using a technology of your choice.

**NOTE** You will not be able to create or modify any IAM resources in this account due to security
limitations. Your contact will be able to make any necessary roles, policies, etc.. that you require,
if you can provide reason for needing them.

## Required Tools

* git
* java
* maven
* junit

## Submitting:

To submit your answer, create a private repository and email that and any instructions for your final submission.
Please do not place any solution in a public git repository or anywhere discoverable by a search engine,
as we want to be able to re-use this test.

