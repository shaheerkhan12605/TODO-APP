# TODO-APP
its a basic TODO APP in Angular JS with basic functionality of add/remove/update TODO List

# Pre-requisite
you only need internet connection to load AngularJS /Bootstrap Cdn
this app is working fine on localhost (I've used Wamp) 

# Service
 I have created a basic service to share /update data of todos list here's the code 
 
 ## app.service('TODOS',function(){
			this.todos=[];
			this.get=function(){
				// alert("IN service")
				return this.todos;
			}
			this.getItem=function(id){
				return this.todos[id];
			}
			this.push=function(item){
				let id=this.todos.indexOf(item)
				if(id==-1){
					this.todos.push(item)
				}else{
					alert("item already exist")
				}
			}
			this.delete=function(item){
				let index=this.todos.indexOf(item);
				this.todos.splice(index,1);
			}
			this.put=function(index,item){
				this.todos[index]=item;
				console.log(this.todos)
			}
		});
##

