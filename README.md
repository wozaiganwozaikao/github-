# github-
github上传项目步骤

1.创建新仓库

Repository name（仓库名称）：为你的仓库起一个简洁明了的名称，最好能够反映项目的性质或用途。
Initialize this repository with a README（使用README初始化仓库）：这是一个很好的习惯，因为README文件通常会包含关于项目的基本信息、如何安装和使用、贡献指南等内容。
Add .gitignore（添加.gitignore文件）：这是一个可选的步骤，但非常有用。.gitignore文件用于指定在提交代码时应该忽略哪些文件或目录，例如编译生成的文件、日志文件等。
Add a license（添加许可证）：为你的项目选择一个合适的许可证，这有助于明确项目的使用、修改和分发规则。
Choose a template（选择模板）：GitHub提供了许多项目模板，可以帮助你快速开始一个新项目。


2.克隆Clone仓库到本地
    
    git clone https://https://github.com/username/repository.git
  
如果设置了SSH密钥 使用ssh来克隆仓库，可以使用

    git@github.com:username/repository.git

3.进入仓库目录开始工作

    cd repository

4.提交和推送代码

  4.1创建README文件
  
    echo "# ros2_rookie" >> README.md # Windows (CMD)
    touch .README.md  # Linux/Mac
     
  4.2初始化git
  
    git init
     
  4.3添加README文件
  
    git add README.md
     
  4.4创建.gitignore文件
  
    touch .gitignore  # Linux/Mac
     
  4.5编辑.gitignore文件
  
      C++
      
     # Build files
       *.o
       *.exe
       build/
       
     Python
     
     # Byte-compiled / optimized / DLL files
      __pycache__/
      *.py[cod]
      
      # Virtual environment
      venv/
      .env/
      
      # Logs
      *.log
      
      ROS2 
      
      # -------------------------------
      # ROS 2 核心构建和开发文件
      # -------------------------------
      # 构建目录（colcon 默认）
      build/
      install/
      log/
      
      # -------------------------------
      # ROS 2 自动生成的文件
      # -------------------------------
      # ament/colcon 生成的文件
      **/*.pyc
      **/__pycache__/
      
      # ROS 2 消息和服务生成的代码
      **/*_msgs/
      **/*_srvs/
      
      # -------------------------------
      # 开发环境和 IDE 文件
      # -------------------------------
      # VSCode
      .vscode/
      
      # CLion/IntelliJ
      .idea/
      *.iml
      
      # -------------------------------
      # 系统/语言相关文件
      # -------------------------------
      # Python
      *.py[cod]
      *.so
      *.egg-info/
      __pycache__/
      
      # C/C++
      *.o
      *.a
      *.so
      *.out
      
      # -------------------------------
      # 日志和临时文件
      # -------------------------------
      *.log
      *.tmp
      *.swp
      *~
      
      # -------------------------------
      # 其他 ROS 2 相关
      # -------------------------------
      # 包缓存
      /.catkin_tools/
      /.ros/
      
      # 仿真和 bag 文件
      *.bag
      *.mcap

  4.6提交gitignore文件
  
     git add .gitignore
     git commit -m "Add .gitignore  # git commit -m "Add ROS 2 specific .gitignore"
     git push
     git status --ignored  # 查看被忽略的文件
     
  4.7更新替换origin远程

      git remote remove origin
      git remote add origin https://github.com/wozaiganwozaikao/ros2_learn_note.git
      git remote -v

      结果正确会显示:
      
      origin  https://github.com/wozaiganwozaikao/ros2_learn_note.git (fetch)
      origin  https://github.com/wozaiganwozaikao/ros2_learn_note.git (push)

  4.8推送代码
  
     #如果分分支是main
      git add .
      git commit -m "first commit"
      git branch -M main
      git push -u origin main
     #如果分支是master
      git push -u origin master
     
指令git add .
只添加特定文件/文件夹
git add folder_name/ #例如 git add src/
