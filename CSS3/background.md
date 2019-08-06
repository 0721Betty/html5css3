#### 添加背景颜色

- background-color: skyblue;

#### 添加背景图片

- background-image:url("../images/1.png");
  - 如果图片大于容器，那么默认从容器左上角开始放置
  - 如果图片小于容器，那么默认会平铺

#### 设置背景的平铺

- **background-repeat**
  - round 会将图片进行缩放后再平铺
  - space 图片不会缩放平铺，只是会在图片之间产生相同的间距值

#### 设置在滚动容器的背景的行为background-attachment

- 跟随滚动（前提是滚动当前容器的内容）
  - scroll：背景图片不会跟随内容一起滚动
  - local：背景图片会跟随内容一起滚动
- 固定fixed

#### background-size设置背景图片的大小

- 宽度/高度   宽度/auto(保持比例自动缩放)，建议在使用这个属性之前先确定图片宽高比与容器的宽高比是否一致，否则会造成图片失真变形  background-size: 300px 500px
- background-size: 50% 50%;设置百分比，是参照父容器可放置内容区域的百分比
- background-size:contain;  按照比例调整图片大小，使用图片宽高自适应整个元素的背景区域，使图片全部包含在容器内
  - 图片大于容器：有可能造成容器的空白区域，将图片缩小
  - 图片小于容器：有可能造成容器的空白区域，将图片放大
- background-size:cover;  cover的效果与contain的效果相反，背景图片会按比例缩放，自适应整个背景区域，如果背景区域不足以包含所有背景图片，图片内容会溢出

#### background-origin设置背景坐标的原点

- border-box:从border的位置开始填充背景，会与border重叠
- padding-box:从padding的位置开始填充背景，会与padding重叠
- content-box:从内容的位置开始填充背景

#### background-clip设置内容的裁切，设置的是裁切，控制的是显示

- border-box:   其实是显示border及以内的内容
- padding-box:    其实是显示padding及以内的内容
- content-box:    其实是显示content及以内的内容