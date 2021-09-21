# TLX Problem Tagging Style Guide

> Available in: English

This document is a convention on how to tag problems in TLX.

## Table of Contents

- [A. Goals](#a-goals)
- [B. Principles](#b-principles)
- [C. Guidelines](#c-guidelines)

## A. Goals

When tagging a problem, it must directly or indirectly achieve the following larger goals:

1. By viewing the list of tags, one can <ins>discover new concepts</ins> that they didn't know before.
2. By clicking on one tag, one can practice with <ins>relevant problems</ins> that use the concepts.
3. By solving problems tagged with a tag, one will <ins>gain more experience</ins> with the concepts.

## B. Principles

1. Tagging problems is inherently a <ins>subjective</ins> activity. It is not uncommon if two people disagree on the set of tags of a problem. As a solution, we have come up with a set of <ins>guidelines</ins> below.
2. It is important to <ins>be consistent</ins> when applying the guidelines. We know that according to some people, the guidelines may not be 100% correct. However, we feel that consistency is more important here.
3. Before tagging, it is recommended to <ins>explore existing</ins> problem tagging in TLX, to see the existing guidelines application in action.

## C. Guidelines

Consider all individual intended solutions. <ins>For each intended solution</ins>, pick one or more tags, according to the following guidelines. Finally, merge all the tags over all solutions as the final set of tags.

1. Most tags are self-explanatory. Pick a tag if the solution uses/needs a knowledge of the concepts of the tag.
2. Some tags can have multiple interpretations. For consistency, here are some guidelines:

   - `implementation`
     * Pick this tag if the solution is to (almost) exactly do what the problem statement <ins>literally says</ins>.
     * Don't pick this tag if there is one or more additional steps/insights needed. This tag is intended for beginners to practice implementing code. 

   - `constructive`
     * Pick this tag if the solution is to <ins>creatively</ins> construct <ins>any solution</ins> which satisfies the provided criteria, out of (usually) many possible solutions.
     * Don't pick this tag if the solution heavily relies on a well-known algorithm/technique. The emphasis here is "creatively".
     * Usually, <ins>interactive</ins> and <ins>output-only</ins> problems will have this tag, because usually it requires creative solutions.

   - `data structure`
      * `:compression`
        * Pick this tag if the solution required "compressing" coordinates / array positions.
      * `:fenwick tree`
        * Pick this tag if the solution can use either fenwick tree or segment tree, e.g. just for <ins>standard range query</ins> capability.
        * If this tag is picked, don't pick the `:segment tree` tag.
      * `:segment tree`
        * Pick this tag if the solution needs segment tree with <ins>lazy propagation</ins>.
      * `:prefix sum`
        * Pick this tag if prefix sum is the <ins>main idea</ins> of the solution.
        * Don't pick this tag if prefix sum is not the main idea. For example:
          * It is just for optimizing larger DP transition.
          * It is used inside `searching: two pointers` solution.
      * `:stack` / `:deque` / `:heap` / `:binary search tree`
        * Pick these tags if they are used for nontrivially as part of a larger solution. Example: stack is used as a monotonic stack to optimize a DP solution.

   - `dynamic programming`
     * `:combinatorics`
       * Pick this tag if the DP is about <ins>counting</ins> number of ways, or a larger solution which needs it, for example:
         * printing the <ins>K-th lexicographically</ins> smallest sequence.
         * computing <ins>probabilities</ins>.
     * `:tree`
       * If this tag is picked, no need to also pick `tree` tag.

   - `heuristic`
     * Pick this tag if the intended solution (leading to full / most of the points) requires a randomized solution.
     * `:las vegas`
       * Pick this tag if the solution uses Las Vegas algorithm, i.e., randomized solution which can be proved to get full points.

   - `math`
     * `:combinatorics`
       * Pick this tag if the problem is about counting number of ways (and solvable without DP).
       * If `dp:combinatorics` is already picked, don't pick this tag.

     * `:number theory`
       * Pick this tag is the problem requires knowledge of properties of integers.

   - `bitwise operation`
     * Pick this tag if the problem description and the solution contain bitwise operations (such as XOR).

3. For each top-level tag, always try to see if a more specific subtag <ins>can</ins> be picked. If so, pick the subtag.
   * Exception: for each of these tags, if it is picked, at least one of its subtags <ins>MUST</ins> be picked. If there is no appropriate subtag, <ins>DON'T</ins> pick the tag at all (because it does not make sense for them to appear on their own).
     * `data structure`
     * `searching`
     * `string`
     * `optimization trick`
   * In any case, if you want to propose a new subtag for a problem, you can raise it [here](https://github.com/ia-toki/tlx-issues).

4. Finally, consider picking the `ad hoc` tag, if the solution does not need prior knowledge of any specific concepts. The guidelines are as follow.
   * ALWAYS pick `ad hoc` tag if the set of picked tags so far (may be empty) is a subset of:
     * `bitwise operation`
     * `constructive`
   * CONSIDER picking `ad hoc` tag if the set of picked tags so far (may be empty) is a subset of:
     * `geometry` (without any subtags)
     * `math` (without any subtags)
      
     , and none of their subtags were picked because the solution actually does not use any specific concepts under those tags.
   * DON'T pick `ad hoc` tag if none of the above conditions are satisifed. 
5. Note that all the above rules apply to each intended solution. There are no rules for tags between two solutions. For example, if there are two possible intended solutions, one uses `dynamic programming` and one uses `ad hoc` (simple observation), it is OK to have {`ad hoc`, `dynamic programming`} as the final tags.

---

This document is written by:

- Ashar Fuadi
