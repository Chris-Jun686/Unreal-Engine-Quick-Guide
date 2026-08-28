# Unreal Engine本地化系统快速导览

## 如何导出需要本地化的文本
1. 打开顶部菜单栏：**工具 -> 本地化控制板 (Localization Dashboard)**。
<img width="930" height="551" alt="3aaae12e34aaa63c463239a166385f6e" src="https://github.com/user-attachments/assets/c36c086b-672c-47f5-b3c2-2e7272f73b9f" />
2. 选择配置搜索范围：</br>
   - **C++ 收集**：选择“从文本文件收集”，搜索目录填写源码所在文件夹；
   - **蓝图收集**：选择“从包收集”，包含路径通配符填写内容浏览器目录；
   - <img width="1678" height="938" alt="686a5f7708f71133a049b977411dcc3e" src="https://github.com/user-attachments/assets/23181406-11b1-4903-b72a-4c626029d8c3" />
3. 配置需要翻译的语种
 <img width="1100" height="1102" alt="e8ca422e2d034e56807fa871146be65a" src="https://github.com/user-attachments/assets/e1a69907-b925-4b6b-b903-a8d7f8bce1b8" />
4. 点击 **收集文本**；
<img width="1056" height="1054" alt="5dd9c76b0e5c6432aad66871d1a0929d" src="https://github.com/user-attachments/assets/d11a1a32-da1f-42d6-8281-aecfdab3ab62" />
5. 收集完成后，在目标语种（如zh-Hans）所在行，点击右侧的 **“导出此语言的翻译”**，引擎将自动生成.po格式的翻译文件；
  <img width="943" height="829" alt="0d1acb510236b795c5870afbd6160436" src="https://github.com/user-attachments/assets/5b336b1c-ed4c-446c-9e34-8941493f767d" />
6. 将生成的.po文件交付给 Orbit8 团队进行翻译和校对。
<img width="1443" height="958" alt="40bf3e00cfd6d4f3839145c3b0da1435" src="https://github.com/user-attachments/assets/eb2888f2-c388-464b-9ccc-5bc950932976" />

## 5. 如何导入翻译后的文本文件

Orbit8 团队翻译完成后，将.po文件交付给开发团队。请严格遵循以下步骤：

1. **文件放置要求**：</br>
确保Orbit8返回的.po文件**命名规范**（如 Game.po），并放置在对应的语言目录下（如 Content/Localization/Game/zh-Hans/Game.po），不要随意修改文件名或路径。
2. **执行导入**：</br>
在 **工具 -> 本地化控制板** 中，**不要在顶部的“导入文本”按钮操作**（该按钮仅用于导入内部 .archive文件）。</br>
   **正确做法**：</br>
   在语言列表中找到目标语种（zh-Hans）那一行，点击右侧的 **“导入此语言的翻译”**，选择翻译后的.po文件即可。
3. **编译文本**：</br>
导入完成后，**务必点击“编译文本”**，以生成.locres二进制文件，随后才能在游戏运行时调用。

## 6. 预期效果（如何验证）

在 **编辑 -> 编辑器偏好设置 -> 区域和语言 -> 预览游戏语言 (Preview Game Language)** 中，切换需要显示的语种（如 zh-Hans），即可在编辑器中实时预览本地化完成的内容。

---



