## 2026-03-20 - [GameObject.Find() Cache Optimization]
**Learning:** [SceneDirector.cs was doing expensive `GameObject.Find()` calls in a loop when spawning characters or applying interactions, which scans the entire scene tree. Unity overrides the == operator for GameObjects, making cached null checks a safe and effective way to see if an object was destroyed.]
**Action:** [Use a `Dictionary<string, GameObject>` to cache GameObjects found or created, substituting repeated `GameObject.Find()` calls with dictionary lookups for faster scene setups.]
