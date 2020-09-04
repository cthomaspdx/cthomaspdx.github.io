---
layout: post
title: "When Containers Click"
date: 2017-06-12 10:05:01 -0700
comments: true
categories:
published: false
---
##Realizing the benifits of application containerization as cloud systems engineers. 


In discussing operations around software web applications, many in the field are still reluctant to move to containers like docker or rkt, and container schedulers like Kubrenetes or Nomad. The benefits of containers just aren't very obvious but the added complexity is. So the reluctance seems justified. Furthermore, the marketing of containers seems to be directed towards developers and the benefits of packaging applications with all of their dependencies in a portable format, ending the "works on my machine" narrative. But as the people in charge of the system and operations people the complexities are real.

 Some operators are still just getting used to idea virtual machines OS on bare metal hardware, and containerization just seems like another virtual machine on top of a virtual machine. Why would we want to add that? What does doing that offer? How do we handle routing when we may not even know where a container is running? Of course each of the problems has a solution but each solution is more complexity. 

But is complexity a bad thing? Lets take the example of a car, sure todays cars are far more complex than cars of the past, so much that many hobbyists can no long work on them, while this is unfortunate, the complexity has created reliability, cleaner running vehicles and ease of use. Containers are not much different in this respect. Yes we can't keep the entire infrastructure in our head but if the patterns consistent and code well documented then we needn't worry as we can know exactly where to look. And deployments are cleaner, scaling is faster and more robust and resource usage is much more manageable. 

Deployments benefit in many ways. The old way to deploy was find a way to push up the new code, clear out the old and restart, and do this across 20 + machines. Weather that be by updating a the code with provisioner and pulling artifacts its artifacts from a repository, this worked great, except when it didn't hunting down the server that for some reason was still serving old code was always a fun chore. Schedulers like nomad along service discovery now take care of that for you, instead of restarting the app you place an entire container and artifacts start it up, kill the old and reroute the traffic to the new. I have yet to track down a bad box when using this methodology. Deployments can be made easily in parallel speeding up the deploy process.  


improving scaling times
cost (bin packing /spot instances/ internal routing)


faster and more reliable deployments and application stability

the bad and ugly (complexity, abstraction)

