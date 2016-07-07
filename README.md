# android-maven-deployer
方便上传本地aar至jcenter

##配置步骤
1、目标module的build.gradle末尾添加：
`apply from: 'https://raw.githubusercontent.com/lintran-cn/android-maven-deployer/master/android-maven-deployer.gradle'`

2、目标module目录下新增gradle.properties文件，文件中配置信息
#项目分组.注意与library的包名一致
PROJ_GROUP=com.example.maven
#项目名称.jcenter中显示的项目名称
PROJ_NAME=maven-example
#项目版本.
PROJ_VERSION=1.0.0

#项目地址
PROJ_WEBSITEURL=https://github.com/lintran-cn/maven-example
PROJ_VCSURL=https://github.com/lintran-cn/maven-example.git

#项目介绍
PROJ_DESCRIPTION= Example project of maven
#项目artifactId.注意需与library的module name一致
PROJ_ARTIFACTID=maven-example

#开发者信息
DEVELOPER_ID=开发者ID
DEVELOPER_NAME=开发者名称
DEVELOPER_EMAIL=开发者邮箱

3、在项目根目录下的local.properties文件中添加配置：
BINTRAY_USER=用户名
BINTRAY_APIKEY=jcenter api key