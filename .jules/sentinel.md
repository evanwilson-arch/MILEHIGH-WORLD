## 2024-11-06 - Prevent Information Exposure via Error Logs in Unity Scripts
**Vulnerability:** Found `CampaignManager.cs` logging exact absolute file paths (using `Application.streamingAssetsPath` and `Application.dataPath`) and lacking exception handling around a JSON read/parse block, potentially leaking system info or stack traces.
**Learning:** Unity's built-in platform paths can expose underlying OS directory structures, usernames, or execution environments when logged directly, especially if logs are captured.
**Prevention:** Mask runtime exception stack traces (e.g. log only `ex.Message`) and replace absolute path logs with safe generic identifiers (like the filename) to avoid information exposure.
