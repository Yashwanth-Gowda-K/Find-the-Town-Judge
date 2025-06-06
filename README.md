# Find-the-Town-Judge


This repository contains a Python solution for the Find the Town Judge problem from LeetCode. The solution efficiently identifies the town judge based on given trust relationships among the townspeople.

Problem Statement
In a town of n people labeled from 1 to n, there is a rumor that one of them is the town judge. The judge is defined by the following properties:

The judge trusts nobody.

Everybody (except the judge) trusts the judge.

There is exactly one person who satisfies these conditions.

Given an array trust where trust[i] = [a, b] means person a trusts person b, determine the label of the town judge or return -1 if no such person exists.

Solution Approach
The solution uses indegree and outdegree counting to determine the judge:

Indegree: Number of people who trust a given person.

Outdegree: Number of people a given person trusts.

Key Insight
The judge must have an indegree of n-1 (trusted by everyone else).

The judge must have an outdegree of 0 (trusts nobody).

Algorithm Steps
Initialize two arrays (indegree and outdegree) to keep track of trust counts.

Iterate through the trust array and update counts.

Check for a person who satisfies indegree[i] == n-1 and outdegree[i] == 0.

Return the judge's label if found, otherwise -1.

Time & Space Complexity
Time Complexity: O(n + t) where t is the number of trust relationships.

Space Complexity: O(n) for storing indegree and outdegree.
