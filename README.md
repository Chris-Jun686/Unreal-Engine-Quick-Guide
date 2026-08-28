# Unreal Engine本地化系统快速导览

## 如何导出需要本地化的文本
1. 打开顶部菜单栏：**工具 -> 本地化控制板 (Localization Dashboard)**。
<img width="930" height="551" alt="3aaae12e34aaa63c463239a166385f6e" src="https://github.com/user-attachments/assets/c36c086b-672c-47f5-b3c2-2e7272f73b9f" />


2. 选择配置搜索范围：</br>
   - **C++ 收集**：选择“从文本文件收集”，搜索目录填写源码所在文件夹；
   - **蓝图收集**：选择“从包收集”，包含路径通配符填写内容浏览器目录；
<img width="1673" height="1073" alt="71ee43a90464cc8fdda3ccd629a86611" src="https://github.com/user-attachments/assets/66283fb8-5c05-4b66-84db-89cfbe37f724" />


3. 配置需要翻译的语种
<img width="1446" height="1034" alt="image" src="https://github.com/user-attachments/assets/c6a8ddc6-967c-4781-9517-bde888cd9195" />
**收集文本前务必先添加需要本地化的语种，否则无法收集到文本** </br>


4. 选择游戏原语言为本地语言，UE默认本地语言为英语
<img width="726" height="123" alt="86b4ef57cde39f2e25bccae9b7d8ee87" src="https://github.com/user-attachments/assets/9fce9ef8-e12d-4d30-9528-0e8aa8317f87" />
  

5. 点击 **收集文本**；
<img width="1580" height="1061" alt="405cb17b85e162d765058eab06de62c6" src="https://github.com/user-attachments/assets/cc3e9089-9bce-47a4-8dea-5b81d5991b8b" />



6. 收集完成后，点击目标语种右侧的 **“导出此语言的翻译”**，引擎将自动生成.po格式的翻译文件；
-<img width="1645" height="1055" alt="image" src="https://github.com/user-attachments/assets/62e007cb-68de-445d-8df2-d92a987dbc36" />


  
7. 将生成的.po文件交付给 Orbit8 团队进行翻译和校对。
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



