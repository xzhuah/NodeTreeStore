# NodeTreeStore Addon Introduction

Developed by [Xinyu Zhu/异次元学者](mailto:xzhuah77@gmail.com)

Supported Blender Version: >= 2.8.0 

支持的Blender版本: >= 2.8.0

Video Demo: https://www.bilibili.com/video/BV1cW4y1T7bV/?share_source=copy_web&vd_source=274308cad241acba810d206ac5a69844

视频演示：https://www.youtube.com/watch?v=Vf-z0z9YHPg&t=3s

## Core Features

### Save and Load Any Nodes
This addon allow you to save any kind of Node Trees in Blender,
including ShaderNode, GeometryNode, CompositorNode and TextureNode, with Json Format.
The saved node trees can be loaded and restored to any other projects.

* Support ShaderNode, GeometryNode, CompositorNode and TextureNode
* NodeGroup, Image Texture Node, Color Ramp, RGB Curves, Frame, Rerouting Points are all supported.
* Provides Cross Blender version support, as long as the Node Type exists in both blender versions. Future blender versions
will also be supported without the need to update the addon, because this addon can pick up Nodes attribute and structure dynamically.


### Special Offers

* Support categorizing your nodes, helps manage large amount of presets.
* Support copy and paste from clipboard, makes workflows more efficient.
* Support two image texture saving strategy.
    * Auto saving will copy the image to add-on resource folder and refer to that image, so you need to worry about moving the image files
    will affects those saved nodes. This is also useful when you wan to share your saved nodes.
    with other people.
    * Non auto saving will use the original image path, more friendly for saving storage space.
    
    
### Out of Scope

* NodeTreeStore won't store reference to objects, scripts and other resources used in nodeTree. Only Image texture are supported. Referenced object will be restored as an empty object, with location ,rotation and scale. Referecend material in Geometry Nodes will also be restored.
* If you use Frame in Frame when doing layout, the location of the Frame might not be recovered correctly.
* Some TextureNodes has special attribute that can't be saved. 

### License

    NodeTreeStore is a blender addon for storing and retrieving any kind of nodeTrees via Json Format.
    It applies GNU General Public License (GPL)
            Copyright (C) 2022  Xinyu Zhu

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.

# 节点树仓库插件介绍

由 Xinyu Zhu/异次元学者 (xzhuah77@gmail.com) 开发
## 核心功能

### 保存和加载各种节点树

这款插件能以Json格式保存Blender中的各种节点树，包括着色器节点，几何节点，合成节点以及纹理节点。
保存的节点可以被轻松地加载到其他项目中。

* 全节点支持: 着色器节点，几何节点，合成节点以及纹理节点
* 完全支持节点组，图片纹理节点，颜色渐变，RGB曲线，框，转接点等特殊节点
* 提供跨Blender版本支持，只要两个Blender版本同时具有某个节点，这个插件便可以在它们之间正确保存和加载这个节点，此插件可以动态读取节点的属性和结构，因此
可以无须更新就能支持未来版本的Blender节点。


### 其他功能

* 支持节点分类，方便保存大量的节点树
* 可以直接复制和粘贴节点，方便在同时在不同Blender项目之间工作
* 提供两种可选的图片保存策略
    * 默认的自动复制模型会将节点树中引用的图片复制到插件的资源目录下，以防止原图片被移动后无法找到，同时方便分享节点预设的同时分享图片资源。
    * 关闭自动复制功能后，插件会仅保存图片的原始路径，节省存储空间。

### 注意事项

* 节点树仓库不会保存节点树引用的对象，文本资源等，它们并不被视为节点树的一部分。只有图片资源被视为节点的一部分。引用的物体将会被还原为空物体，保留位置，旋转和缩放信息，几何节点引用的材质也可以被还原。
* 布局时，如果你在一个框里面套另一个框，可能会导致节点的位置信息无法被正确恢复。
* 一些纹理节点具有特殊的属性，可能无法被保存

### 使用许可证

    节点树仓库是一款Blender插件，通过Json格式存储和加载任意形式的Blender节点树，使用请遵守GNU通用公共许可证
    Copyright (C) 2022  Xinyu Zhu
   
    节点树仓库是自由软件：你可以再分发之和/或依照由自由软件基金会发布的 GNU 通用公共许可证修改之，无论是版本 3 许可证，还是（按你的决定）任何以后版都可以。 
    发布节点树仓库是希望它能有用，但是并无保障;甚至连可销售和符合某个特定的目的都不保证。请参看 GNU 通用公共许可证，了解详情。
    你应该随程序获得一份 GNU 通用公共许可证的复本。如果没有，请看 <https://www.gnu.org/licenses/>。
