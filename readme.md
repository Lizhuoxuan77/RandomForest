# 样例





```java

public class Test {
    public static void main(String[] args) throws Exception {
        File train = new File("D:\\User\\学习文件\\新闻分类\\训练数据\\data.csv");
        File test = new File("D:\\User\\学习文件\\新闻分类\\测试数据\\data.csv");
        /**
         * RandomForestTrain类 是用来训练模型的类
         * 调用里面的createForest(File trainDataFile, File testDataFile, Integer treeAmount,String outputPath)方法开始训练模型。
         * 其中参数 trainDataFile：训练数据文件。
         * testDataFile：测试数据文件，主要用于过拟合处理。
         * treeAmount：森林中树的数量。
         * outputPath:模型输出路径
         */
        RandomForestTrain randomForestTrain = new RandomForestTrain();
        randomForestTrain.createForest(train, test, 100, "D:");//D:文件下输出模型文件为model.txt
    }
}
```

```Java
    public void test() throws IOException {
        File model=new File("D://model.txt");
        RandomForestClassification classification=new RandomForestClassification(model);
        String type = classification.ClassificationNew("加快三百多斤卡布达看不看得吧背带裤吧唧的不卡说不定卡不卡的版块把鼠标垫卡布达把看不到", 88);
    }//RandomForestClassification类 是一个分类器类，构建一个RandomForestClassification类对象要传入一个模型文件
```

