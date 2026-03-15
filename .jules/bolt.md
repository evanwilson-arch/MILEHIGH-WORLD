## 2025-03-15 - [Coroutines in Unity Cinematics]
**Learning:** Unity coroutine `new WaitForSeconds()` creates a new object instance every time it's called, causing GC pressure during long sequences.
**Action:** Cache the yield instructions or use constant values in long coroutines/cinematics to avoid allocating memory for short delays repeatedly.
