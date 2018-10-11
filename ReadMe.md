### 工程下多个APP
        
            这是相对基础的知识，只是平时相对比较少用（因为不了解这块知识）。现在在此做下记录，方便以后随时查看。
        诚然了解这款知识后，也不会忘记。
        
#### 如何实现：

        在工程下添加module，在添加的时候选择Phone & Tablet Module，之后的操作就和创建新项目无差异。
        
#### 注意
    
            如果出现Error:Execution failed for task ':secondapp:preDebugAndroidTestBuild'.
        > Conflict with dependency 'com.android.support:support-annotations' in project 
        ':secondapp'. Resolved versions for app (26.1.0) and test app (27.1.1) differ. 
        See https://d.android.com/r/tools/test-apk-dependency-conflicts.html for details.类似错误，
        请在相关module的build.gradle中添加
            configurations.all {
                resolutionStrategy.force 'com.android.support:support-annotations:27.1.1'
            }
        
#### 效果
![效果一](https://github.com/Wzhixiang/MultiProject/blob/master/ScreenCapture/one.png)
![效果二](https://github.com/Wzhixiang/MultiProject/blob/master/ScreenCapture/two.png)
