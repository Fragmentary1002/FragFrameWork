这是我预建立的unity代码框架库

# 文件目录

|      目录       |                             说明                             |
| :-------------: | :----------------------------------------------------------: |
|      ABRes      | 自定义资源目录，用于存放需要动态加载的AB包中的资源。职责类似于Artwork,需要热更新的放入该文件夹并打包. |
|     Artwork     | 存放美术资源的目录（涵盖动画、模型、材质、Shader、UI、原图等等），最好通过 svn 外链或者 git submodel 的方式引入，同样在上面的目录少了一个策划的目录，其实一般就是一个 csv 目录，一般也是通过 svn 外链或者 git submodel 的方式引入 |
|     Editor      | 编辑器目录，存放扩展编辑器的代码，该代码可调用Unity Editor的API。该目录中的代码不会被打进最终的包内。例如，自定义打包工具的代码就放在此目录中。 |
|    External     | 这个目录主要是放置一些外部的插件 Package，例如腾讯的行为树插件，注：外部的 Package 很多代码结构都比较混乱，特别是美术 Package，无论是程序还是美术 Package，请注意都要自己理解透，在按照自己的项目结构整理进对应的目录，如果是代码，不建议整合进自己的项目 |
|     Gizmos      | Gizmos绘图相关的资源放这里，绘制的效果不会在Game视图中显示，除非在Game视图中勾选Gizmos。该目录的资源不会被打进最终的包内。 |
|     Plugins     | 插件目录，用于存放第三方SDK库文件，如微信开放平台的SDK。子目录包括Plugins/Android和Plugins/iOS。此外，还可以存放其他第三方库，如HoTween.dll、Zxing.dll、Ionic.Zip.Unity.dll等。 |
|    Resources    | 资源目录，用于存放需要动态加载的资源。该目录下的所有文件都会自动打进包内，并执行资源压缩。资源文件通过Resources.Load接口进行加载。这是一个只读的文件夹，程序运行时只能读不能写。 |
| StreamingAssets | 流式资源目录，该目录下的所有文件都会自动打进包内，但不会被压缩。它是一个只读的文件夹，程序运行时只能读不能写。可以使用Application.streamingAssetsPath访问该路径。通常用于存放AssetBundle文件。 |
|     Scripts     | 脚本目录，用于存放C#游戏脚本。注意，如果是编辑器工具类的C#脚本，则放在Editor目录中。 |
|     Scenes      | 场景目录，用于存放场景文件，包括场景的Lighting灯光烘焙数据、Navigation导航数据等。 |
|     Shaders     | 着色器目录，用于存放shader文件。Shader一般是技术美术来写，涉及到一些艺术表现效果。 |
|    RawAssets    | 生肉资源目录（自定义），用于存放未加工的资源，如骨骼、动画、贴图、材质等依赖文件。这些资源会作为熟肉资源（预设）的依赖项。 |
|   GameAssets    | 熟肉资源目录（自定义），用于存放已加工过的资源，如预设。通常会将该目录中的资源打成AssetBundle并放在StreamingAssets目录中。在编辑器环境下，可以使用AssetDatabase.LoadAssetAtPah直接加载该目录中的资源。 |



# 在ArtWork下的美术资源文件：



| 目录        | 说明                                                         |
| ----------- | ------------------------------------------------------------ |
| Animations  | 动画相关的资源文件。                                         |
| Animators   | 动画控制器相关的资源文件。                                   |
| Audios      | 音频相关的资源文件。                                         |
| Environment | 存放与环境相关的资源文件，如背景、建筑物、地形、天空、树木、水体等。 |
| Effects     | 存放与特效相关的资源文件，比如粒子系统，摄像头渲染特效，动作特效，技能特效，画面特效等。 |
| Materials   | 材质相关的资源文件。                                         |
| Models      | 模型相关的资源文件。                                         |
| Prefabs     | 预制体相关的资源文件。                                       |
| Sprites     | 精灵相关的资源文件。                                         |
| Shaders     | 着色器相关的资源文件。                                       |
| Textures    | 纹理相关的资源文件。                                         |
| UI          | 存放与游戏界面（UI）相关的资源文件，如按钮、图标、输入框、列表等。 |

# FrameWork文件夹

- XFramework : XF UI框架
- QFrameWork : QF 框架基础1000行
- ProjectBase : 基础框架(自己实现)
  - AssetBundle: AB包管理器
  - AStar : A星算法
  - Base  ：关于单例模式的实现
  - DataSave: 可持续化数据存储管理类
  - Event：事件中心
  - Input： 输入管理类
  - Mono： 基础管理类 可持续化
  - Music ： 音效管理类
  - Pool ： 对象池
  - Res ：Resources文件夹加载
  - Scenes ：场景管理类
  - UI ： UI管理
