vuex 是什么？
  vuex是vue配套的公共数据管理工具 我们可以将数据保存到vuex 中。 
   vuex 是用来存储用户数据的工具

使用vuex 首先1.引入 vuex.js文件
					
	2.在script 中new一个实例Vuex对象
const store=new Vuex.store(｛
								state：｛｝，
	mutations:{}

｝）
	3.然后再挂载在根组件上 那么这样就可以使用vuex 

	如果想要使用vuex中的数据 那么就需要是this.$store.state 就可以使用vuex 中的数据	

	如果想修改数据 不能直接修改state中的数据 在我们创建的vuex对象中 有一个mutation（用于保存修改共享数据的方法） 我们通过在mutation 中创建一个方法 方法的参数是state 修改state 中的数据 

注意点：在纸箱mutation中定义的方法的时候 系统会自动给这些方法传递一个参数state
     如何在组件当中使用mutation的 方法呢 使用this.$store.commit("参数是mutation中的方法名") 

	vuex中的getter？
      vuex 中的getters 属性就和组件中的计算属性一样 会将数据缓存起来 只有数据发生变化才会重新计算.

       getters是用来对于state中的数据进行加工的.
      
      用法：在getters中添加一个方法 同样系统自动有一个参数state 直接return 然后进行操作
     getters:{
    add(state){
       return state.msg
}

   怎么调用getters中的 方法呢 
     this.$store.getters.add
}																																																																																																																																																																																								
					

