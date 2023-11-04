
## 多反应堆+线程池的高并发 HTTP 服务器  
本项目实现了一个多反应堆的高并发网络服务器。该 HTTP 服务器并发处理客户端对静态资源的请求，并且在服务器端采用多反应堆和线程池技术加快响应处理速度。  

### 应用技术
Linux、C++、Socket、TCP、Epoll、HTTP协议、线程池。  
### 主要工作
1、利用 IO 复用技术 Epoll 与线程池实现多线程的 Reactor 高并发模型；  
2、设计多反应堆模式提高服务器端的处理效率，并且解决了惊群问题；   
3、有限状态机解析 HTTP 对静态资源的 get 请求，并将文件映射至内存提高文件的访问速度；  
4、经Webbench压力测试可以实现100万的并发连接。  

### 个人收获
个人对于HTTP的服务过程有了更清晰的认识，对于TCP和IO 多路转接也有了一定的理解。  
