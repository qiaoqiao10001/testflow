# testflow
使用git flow 步骤

1. 在仓库中 git flow init 
   - 一路回车就行，这个命令相当于写入一些默认命令流程到.git中, 此命令执行之后会增加develop分支
2. 需要开发新功能 使用git flow feature start <feature_name> 
  - 本命令会创建一个 feature/feature_name的分支, 可以在此分支上 `git add .` 和 `git commit -m 'xx'` 来不断提交修改代码
3. 完成开发 `feature/feature_name` 分支之后，使用`git flow feature finish  <feature/feature_name>` 来完成功能分支的合并，此时feature会被合并到develop分支，并且此分支会被删除
4. 当完成所有功能开发之后使用 git flow release start <1.0.0> 创建release分支，发版分支，这时会触发构建
5. 创建完成之后使用`git release finish '1.0.1'` 把realease合并到master 这样master就拥有了测试过的，修复完bug的所有代码了；

