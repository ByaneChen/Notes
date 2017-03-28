# SpringAnimation

Android在25.3.0的support包中添加的动画支持，模拟类似弹簧的效果。

# Sample
	
	//给`box`这个view增加水平方向的弹簧效果动画，最终回到起始位置：
	SpringAnimation animX = new SpringAnimation(box, SpringAnimation.TRANSLATION_X, 0);
	
	//刚度设置为0.3f
	animX.getSpring().setStiffness(0.3f);
	
	//阻尼系数设置为0.5f
	animX.getSpring().setDampingRatio(0.5f);
	
	//设置起始速度为每秒移动3个元素宽度
	animX.setStartVelocity(3*resources.getDimensionPixelOffset(R.dimen.org_cici_ps__widget_size_32));
	
	//开始动画
	animX.start();


# SpringForce

`SpringAnimation.getSpring()` 返回`SpringForce`类型的对象，可以通过它设置弹簧动画的效果。

* 设置刚度

		SpringForce setStiffness(float stiffness)

	stiffness的值越大，则表示弹簧约紧绷，可伸展的范围越小；这个值越小，则表示弹簧约松散，可以伸展得越远；
	
* 设置阻尼系数

		SpringForce setDampingRatio(float dampingRatio)
		
	dampingRation越小，则表示阻尼越小，弹簧震荡的次数越多，范围越大
	
	
* 设置最终位置

		SpringForce setFinalPosition(float finalPosition)





# Reference

* [官方文档](https://developer.android.com/reference/android/support/animation/SpringAnimation.html)
* [Github非官方Demo](https://github.com/brucevanfdm/SpringAnimation)