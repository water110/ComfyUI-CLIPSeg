#### Thanks:
# [ComfyUI-CLIPSeg](https://github.com/biegert/ComfyUI-CLIPSeg/tree/main)
# [所需模型文件](https://huggingface.co/CIDAS/clipseg-rd64-refined/tree/main)
#### 因为模型文件较大，故pytorch_model.bin未上传，请到以上网址下载

1、如果直接将原作者的代码下载到本地，作为comfyui自定义节点运行的话，会报错提示没有__init__.py文件，原作者的方法是需要将clipseg.py放在custom_nodes文件夹下才可运行，因为此文件中已经包含了初始化的说明，所以才可以按照作者的方法进行正常运行；

2、对于像我一样的强迫症患者，将PY文件直接放在custom_nodes文件夹下，让我很不舒服，所以我还是创建了一个自定义节点的文件夹：ComfyUI-CLIPSeg，然后将clipseg.py放在此文件夹下，然后新增了__init__.py文件，放置在此文件夹下，这样就可以正常运行了；

3、原作者将此节点需要用到的模型放置在comfyui根节点下的CIDAS——》clipseg-rd64-refined，这样不利于模型文件的统一管理，作为强迫症的我，在models下新建了一个clipseg的文件夹，用于存放需要用到的模型文件，此时需要修改clipseg.py中的模型引用路径，因为网络原因，故将此模型文件保存至本地，便于离线使用；

4、原作者还提到一个因为相关依赖库版本升级问题，优化了部分代码，此代码也已更新；

5、原作者requirements.txt中依赖的库都是指定固定版本，有较大兼容性问题，故修改为大于等于以上版本即可；

###其他疑难问题，可参考以下相关链接###

1、ComfyUI ClipSeg插件报错- CV2错误，https://www.bilibili.com/video/BV1sb421Y7tw/?spm_id_from=333.337.search-card.all.click&vd_source=278bda11b78e5becb7b9c6efd408df5b

2、ComfyUI ClipSeg插件报错- resize_image出错应该怎么办，https://blog.csdn.net/JuMengXiaoKeTang/article/details/137383951

3、Comfyui插件CLIPSeg应该如何安装，https://blog.csdn.net/JuMengXiaoKeTang/article/details/137380474

4、ComfyUI-CLIPSeg原作者，https://github.com/biegert/ComfyUI-CLIPSeg

最后补充说明下，我不是专业的计算机编程从业者，只是一名comfyui的爱好者，所以以上建议可能并不专业，欢迎指正不对之处和提出宝贵意见，希望可以帮助到大家！
