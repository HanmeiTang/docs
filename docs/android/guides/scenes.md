---
id: android-scenes
title: 场景管理
---

## 相关类

首先，我们需要知道场景类： `SceneState` 和 `PptPage` 类。

>请注意：SDK中的类，都是配置数据，用于向白板传递数据用，并不持有任何白板实例

### PptPage 类

PptPage 类，是 ppt 相关的配置信息。在创建 WhiteScene 类时传入，再通过插入场景 API时，生成带背景图片的白板页面。

```Java
public PptPage(String src, Double width, Double height)
```

图片中心为白板页面的中心点。

### Scene 类

```Java
public Scene(String name, PptPage ppt)
```

WhiteScene 管理了一个白板页面，其中包含了 name，并且接管了原来的 ppt 内容。
白板页面只有在创建时，才接受 ppt 参数。

### SceneState 类

```Java
public class SceneState {

    //当前场景目录下，所有的页面
    public Scene[] getScenes() {
        return scenes;
    }

    //当前场景路径
    public String getScenePath() {
        return scenePath;
    }

    //当前场景在 Path 中的索引
    public int getIndex() {
        return index;
    }
}
```

该类描述了当前场景目录的状态。

## API 介绍

请查看 [进阶文档-场景管理](/docs/advance/advance-scenes)