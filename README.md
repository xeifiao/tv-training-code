# tv-training-code
torchvision对象检测微调教程  https://pytorch.org/tutorials/intermediate/torchvision_tutorial.html
https://pytorch.apachecn.org/#/docs/1.7/19


将官方的一个函数替换，程序便正常运行


def get_transform(train):
    transforms = []
    transforms.append(T.PILToTensor())
    transforms.append(T.ConvertImageDtype(torch.float))
    if train:
        transforms.append(T.RandomHorizontalFlip(0.5))
    return T.Compose(transforms)

其中用到的transforms utils，见 detection文件夹

