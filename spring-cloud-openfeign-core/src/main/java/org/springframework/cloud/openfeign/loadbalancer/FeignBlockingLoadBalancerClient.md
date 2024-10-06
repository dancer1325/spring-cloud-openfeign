* == implementation of "feign.Client" /
  * | SAME time
    * resolve the request host 
    * use `LoadBalancerClient` -- to select a -- `ServiceInstance`
* TODO: