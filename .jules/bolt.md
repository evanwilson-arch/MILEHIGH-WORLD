## 2024-05-24 - Unity GameObject.Find Bottleneck
**Learning:** `GameObject.Find` is heavily used in setup scripts like `SceneDirector.cs` which can cause significant frame drops during scenario initialization or interaction processing. Unity's overridden `!= null` check works properly for detecting destroyed objects in a Dictionary cache.
**Action:** Always consider replacing `GameObject.Find` inside loops or repetitive functions with a cached Dictionary approach in Unity C# scripts.
