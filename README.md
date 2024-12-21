# Kotlin removeIf() Gotcha: In-Place Modification and Unexpected Behavior

This repository demonstrates a potential issue when using the `removeIf()` function in Kotlin.  While `removeIf()` offers a concise way to remove elements from collections, its in-place modification can lead to unexpected behavior if not carefully considered.

## The Problem

The `removeIf()` function modifies the collection directly.  This can cause issues when combined with other operations that iterate over or depend on the original state of the collection, leading to unexpected omissions or exceptions. 

## Solution

The solution involves making a copy of the collection before using `removeIf()` if you need to preserve the original collection's state.  Alternatively, consider alternative approaches that don't modify the original collection in place.