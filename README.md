# tomcat8-redis-session
这个代码是在原作者https://github.com/jcoleman/tomcat-redis-session-manager
的基础上修改，原作者的不支持tomcat8,所以参考网上的教程，自己修改了相应的代码；
代码的修改只有一处：
将作者原来的RedisSessionManager.java里的initializeSerializer()方法里的
    if (getContainer() != null) {
     loader = getContainer().getLoader();
    }    
注释掉
修改为如下代码：
Context context = this.getContext();
    if(context!=null){
    	loader = context.getLoader();
    }
 本机测试已通过；
 

