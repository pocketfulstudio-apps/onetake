# OneTake TestFlight — Detailed tester SOP

## English

### Purpose and sequence

Test the photo-review workflow and the entitlement sequence **one Free scan of photos from the past year → purchased Lite → Max trial → purchased Max**. Complete and review the Free scan before buying Lite or starting any trial. Then follow the purchase sequence; buying Max first prevents starting the trial.

**Both Lite and Max purchases are FREE in TestFlight.** Displayed prices are part of purchase testing. Use the beta installed through TestFlight. Test purchases do not carry over to the App Store release. [Apple's guidance](https://developer.apple.com/in-app-purchase/)

### 1. Prepare

1. Open TestFlight and install/update OneTake to the requested beta build.
2. Record the build number, iPhone model, iOS version and test date.
3. Prepare a few groups of similar, disposable photos. Use these for deletion tests.
4. Start on Free, before purchasing Lite or Max or starting the trial. If the trial is unavailable, report the condition; it is stored across reinstalls.

**Pass:** The beta opens and the starting tier and trial eligibility are recorded.

### 2. Authorise photo access

1. Tap **Allow photo access**.
2. Choose Full Access for the library, or select specific photos.
3. If access was denied, tap **Open Settings** and update the photo permission.
4. With limited access, verify the app explains that only selected photos are included. Use **Choose more photos** to expand the selection when needed.

**Pass:** The home screen appears and the intended test photos are accessible.

### 3. Complete one Free scan of the past year

1. Verify Free shows up to **3 sets and 1 scan per day**. Free cleaning covers photos from the past year.
2. Choose **Scan range → Last year**. This first scan must cover photos from the past year.
3. Choose **Match → Normal**. Strict finds closer matches; Loose groups a broader range of same-scene shots.
4. Tap **Scan Photos once** while still on Free, and keep the app open until the results appear. Do not buy Lite or start the trial before this scan finishes.
5. Record the scanned photo count and sets found. Review the results before upgrading. If none appear, record that outcome and check permissions, date range and photo suitability; continue to Lite before running another scan.

**Pass:** Exactly one scan was completed on Free with Last year selected, and its result was reviewed before any upgrade. Scanning alone does not delete photos.

### 4. Review, keep, skip and delete

1. Open a set under **All**.
2. Tap thumbnails to browse. Tap **Zoom in**, then pinch or double-tap to inspect details; swipe between photos. For Live Photos, press and hold to replay motion.
3. If needed, use **View in All Photos (what's before and after)**, then close it to return.
4. Check each marker: checkmark means keep; trash icon and dimming mean delete. **Tap the large preview to change its selection.** Thumbnail taps only change the displayed photo.
5. Test **Keep all → Next** on one set, and **Skip** on another. Both retain the photos and put the reviewed set into skipped sets.
6. On a disposable test set, mark only unwanted photos. Check the keeping count and **Delete [number]**.
7. Tap Delete, cancel Apple's prompt once, and verify nothing was deleted.
8. Repeat Delete and confirm Apple's prompt. Verify the intended photos remain and the app advances.
9. Tap **Done**. Reopen available results using **See last results** without spending another scan.

**Pass:** Selections are clear, cancellation preserves photos, and confirmed deletion affects the intended photos only.

### 5. Test purchase Lite — FREE in TestFlight

1. Only after completing the Free scan of the past year and reviewing its result, open Home → settings → **Upgrade / trial**; alternatively tap the allowance chip.
2. Do **not** start the trial yet. Scroll past the trial and Max cards to Lite.
3. Tap **Get Lite** and complete Apple's test purchase confirmation.
4. Check the **Lite is unlocked.** confirmation. Dismiss it and check Lite's button reads **Owned**.
5. Close the upgrade screen. Verify Home shows **Lite**, 5 sets and 5 scans a day, less any already used that day.
6. Choose **Scan range → All photos** and verify it is available.
7. Open settings → **Skipped sets → Show these sets again**. Verify the skipped sets return to scanning. This action restores all skipped sets to review; it does not recover deleted photos.

**Pass:** Lite is owned; older-photo access and restoring skipped sets are unlocked.

### 6. Start and test the three-day Max trial

1. Reopen **Upgrade / trial**.
2. Tap **Start free trial** under **Try Max free for 3 days**.
3. Verify Home shows **Max** and **trial until [date]**. Record the displayed end date.
4. Choose **Scan range → Custom dates**, set **From** and **To**, and tap **Done**. Both dates are included.
5. Scan the test photos and inspect the **Smart pick** suggestion where shown. Review it rather than assuming it is your preferred shot.
6. Open results and inspect Mega clean. Read the counts and keeping rule before confirming any deletion; use only disposable photos for this test.
7. If matching-duration Live sets exist, inspect **Same-length Live**. Equal video duration is a grouping signal, not proof of identical content.

**Pass:** A dated Max trial is visible and Max-only features are available.

**Trial expiry expectation:** Because Lite was purchased first, the app should return to Lite if the trial expires before buying Max. Record any screen that incorrectly says it will return to Free. Do not wait for expiry before the next step.

### 7. Test purchase Max — FREE in TestFlight

1. During the active trial, reopen **Upgrade / trial**.
2. Tap **Get Max** and complete Apple's test purchase confirmation.
3. Check the **Max is unlocked.** confirmation, then dismiss it.
4. Check Max's purchase button reads **Owned**. The Max tier label alone is insufficient because trial access already displayed Max.
5. Close and reopen OneTake. Check Max remains owned and Max features remain available.

**Pass:** Max purchase is explicitly confirmed and its card shows Owned, independently of the active trial.

### 8. Restore and verify

1. Open **Upgrade / trial → Restore purchases**.
2. Complete any expected Apple test prompt and verify **Restored Max.**
3. Check the intended kept photos remain. For accidental deletion, check Recently Deleted in Apple Photos promptly.
4. Treat **Freed** and **Can free** as indicative figures, not a measurement of immediately available device storage.

**Pass:** Restore recognises purchased Max and retained photos are intact.

### 9. Report the outcome

Submit TestFlight feedback with build number, phone/iOS, starting state, exact steps, expected result, actual result and relevant screenshot/video. Record each checkpoint separately: **Lite owned; trial active with end date; Max owned; Max restored; photo review/deletion correct**. If purchase or trial eligibility blocks the sequence, report it rather than skipping ahead and claiming a pass.

## 中文

### 目的及操作顺序

测试照片整理流程，以及 **免费版完成一次近一年照片查找 → 已购买 Lite → Max 试用 → 已购买 Max** 的权限变化。先完成并查看免费版查找结果，再购买 Lite 或开始任何试用。随后按指定购买顺序操作；先购买 Max 后将无法开始试用。

**TestFlight 内测试购买 Lite 和 Max 均为免费，不会实际扣款。** 显示价格属于购买流程测试。请使用通过 TestFlight 安装的测试版；测试购买记录不会转入 App Store 正式版。[Apple 官方说明](https://developer.apple.com/in-app-purchase/)

### 1. 测试前准备

1. 打开 TestFlight，安装或更新 OneTake 至指定构建版本。
2. 记录构建版本、iPhone 型号、iOS 版本及测试日期。
3. 准备几组可丢弃的相似照片，用于测试删除。
4. 测试起点应为免费版，尚未购买 Lite 或 Max，也尚未开始试用。如无法开始试用，请记录；试用记录在重新安装后仍会保留。

**通过标准：** 测试版正常打开，已记录起始版本及试用资格。

### 2. 授权照片访问

1. 点击「允许访问照片」。
2. 选择完全访问，或仅授权指定照片。
3. 如此前拒绝授权，点击「打开设置」，修改照片权限。
4. 在有限访问模式下，检查应用是否说明仅处理已授权照片；必要时点击「选择更多照片」增加范围。

**通过标准：** 进入首页，所需测试照片可以访问。

### 3. 用免费版完成一次近一年照片查找

1. 检查免费版每日额度：最多清理 3 组、查找 1 次；可清理近一年照片。
2. 选择「查找范围」→「近一年」。首次查找必须使用近一年范围。
3. 选择「匹配方式」→「标准」。「严格」用于更接近的匹配；「宽松」用于范围更广的同场景匹配。
4. 在免费版中点击「查找相似照片」一次，保持应用打开，等待完成。在此次查找结束前，不要购买 Lite 或开始试用。
5. 记录扫描数量及照片组数，升级前先查看结果。如无匹配，记录该结果，并检查授权、日期范围及照片是否适合；购买 Lite 后再进行新的查找。

**通过标准：** 免费版已按「近一年」范围完成一次查找，并在任何升级前查看结果。查找本身不会删除照片。

### 4. 测试查看、保留、跳过及删除

1. 在「全部」中打开一组照片。
2. 点击缩略图切换照片；点击「放大」后双指缩放或轻点两下检查细节，左右滑动比较。实况照片可按住重播动态内容。
3. 必要时点击「查看相册，看看前后拍了什么」，查看后关闭并返回。
4. 核对标记：对勾表示保留；垃圾桶及变暗画面表示待删除。**轻点大图才会切换保留／删除状态。** 缩略图点击仅切换当前查看的照片。
5. 对一组测试「全部保留」→「下一组」，对另一组测试「跳过」。两者均保留照片，并将已审核照片组加入跳过列表。
6. 对可丢弃的测试照片组，仅标记不需要的照片，核对保留数量和「删除 [数量] 张」。
7. 点击删除，先取消一次 Apple 系统提示，检查没有照片被删除。
8. 再次点击删除并确认系统提示，检查应保留的照片仍在，应用进入下一组。
9. 点击「完成」。通过「继续整理上次结果」重新打开可用结果，检查不消耗新的查找次数。

**通过标准：** 标记清晰，取消时照片不变，确认后仅删除指定照片。

### 5. 测试购买 Lite — TestFlight 内免费

1. 仅在完成免费版近一年查找并查看结果后，进入首页设置菜单 →「升级或免费试用」，或点击额度提示。
2. 此时先不要开始试用。向下滚动，经过试用及 Max 卡片，找到 Lite。
3. 点击「解锁 Lite」，完成 Apple 测试购买确认。
4. 检查「已解锁 Lite。」提示，关闭提示后，确认 Lite 按钮显示「已解锁」。
5. 关闭升级页面，确认首页显示 Lite、每天可清理 5 组、查找 5 次；当日已用的会从额度中扣除。
6. 选择「查找范围」→「全部照片」，确认功能可用。
7. 打开设置 →「暂时跳过的照片组」→「重新整理这些照片组」，检查跳过的照片组重新参与查找。此操作作用于全部跳过的照片组，并非恢复已删除照片。

**通过标准：** Lite 已购买，旧照片访问及重新整理跳过照片组功能已解锁。

### 6. 开始并测试三天 Max 免费试用

1. 再次打开「升级或免费试用」。
2. 在「免费试用 Max 3 天」卡片中点击「开始免费试用」。
3. 确认首页显示 Max 及「试用将于 [日期] 结束」，记录结束日期。
4. 选择「查找范围」→「自选日期」，设置起始和结束日期，点击「完成」。起止日期均包含在范围内。
5. 查找测试照片，在出现「智能优选」时检查其建议，仍需自行判断要保留的照片。
6. 在结果页检查批量清理功能。确认删除前，先阅读照片数量、组数及保留规则；仅使用可丢弃照片进行此项测试。
7. 如存在同时长实况照片组，检查「同时长实况」筛选。视频时长相同只是分组依据，不代表内容完全相同。

**通过标准：** 显示带结束日期的 Max 试用，Max 专属功能可用。

**试用到期预期：** 已先购买 Lite，因此如在购买 Max 前试用到期，应恢复为 Lite。如页面错误提示会恢复免费版，请记录反馈。下一步无需等待试用到期。

### 7. 测试购买 Max — TestFlight 内免费

1. 在试用期间再次打开「升级或免费试用」。
2. 点击「解锁 Max」，完成 Apple 测试购买确认。
3. 检查「已解锁 Max。」提示并关闭。
4. 确认 Max 购买按钮显示「已解锁」。仅看到 Max 版本标签不能证明购买成功，因为试用期间已经显示 Max。
5. 关闭并重新打开 OneTake，检查 Max 仍已购买，相关功能继续可用。

**通过标准：** 已明确确认 Max 购买成功，且购买卡片显示已解锁，不仅是试用中的 Max 权限。

### 8. 恢复购买及最终检查

1. 打开「升级或免费试用」→「恢复购买」。
2. 按需完成 Apple 测试提示，检查「已恢复 Max。」提示。
3. 确认应保留的照片仍在；如误删，尽快到 Apple「照片」应用的「最近删除」检查。
4. 将「已腾出」「还能腾出」作为参考，不视为设备即时可用空间的直接测量。

**通过标准：** 恢复购买可识别 Max，应保留的照片完整。

### 9. 提交测试结果

通过 TestFlight 提交构建版本、手机／系统、起始状态、准确步骤、预期结果、实际结果及必要截图／录屏。分别记录以下检查点：**Lite 已购买；Max 试用已开始且有结束日期；Max 已购买；Max 已恢复；照片审核及删除正确**。如购买或试用资格阻碍指定顺序，请报告问题，不要跳过后声称测试通过。
