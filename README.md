# testflow
使用git flow 步骤

1. 在仓库中 git flow init 
   - 一路回车就行，这个命令相当于写入一些默认命令流程到.git中,此命令执行之后会增加develop分支
2. 需要开发新功能 使用git flow feature start <feature_name> 
  - 本命令会创建一个 feature/feature_name的分支
3. 在feature/feature_name中commit开发并且commit代码，完成功能之后使用 git flow release start <1.0.0> 创建release分支

