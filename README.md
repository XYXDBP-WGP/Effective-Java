# 《Effective Java》

# **第二章：创建和销毁对象**

本章的主题是创建和销毁对象：何时以及如何创建对象，何时以及如果避免创建对象，如果确保它们能够适时的销毁，以及如何管理对象销毁之前必须进行的各种清理。

[第1条 ：用静态工厂方法代替构造器](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC1%E6%9D%A1%20%EF%BC%9A%E7%94%A8%E9%9D%99%E6%80%81%E5%B7%A5%E5%8E%82%E6%96%B9%E6%B3%95%E4%BB%A3%E6%9B%BF%E6%9E%84%E9%80%A0%E5%99%A8%20a66be40052bd46948c65245d141b40af.md)

[第2条： 遇到多个构造器参数时要考虑使用构建器](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC2%E6%9D%A1%EF%BC%9A%20%E9%81%87%E5%88%B0%E5%A4%9A%E4%B8%AA%E6%9E%84%E9%80%A0%E5%99%A8%E5%8F%82%E6%95%B0%E6%97%B6%E8%A6%81%E8%80%83%E8%99%91%E4%BD%BF%E7%94%A8%E6%9E%84%E5%BB%BA%E5%99%A8%206e4a37347e204acf95925018edf5fcfd.md)

[第3条：用私有构造器或者枚举类型强化Singleton属性](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC3%E6%9D%A1%EF%BC%9A%E7%94%A8%E7%A7%81%E6%9C%89%E6%9E%84%E9%80%A0%E5%99%A8%E6%88%96%E8%80%85%E6%9E%9A%E4%B8%BE%E7%B1%BB%E5%9E%8B%E5%BC%BA%E5%8C%96Singleton%E5%B1%9E%E6%80%A7%20b6d2a1f04a2349fd9e9d9ee22b9e6255.md)

[第4条：通过私有构造器强化不可实例化的能力](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC4%E6%9D%A1%EF%BC%9A%E9%80%9A%E8%BF%87%E7%A7%81%E6%9C%89%E6%9E%84%E9%80%A0%E5%99%A8%E5%BC%BA%E5%8C%96%E4%B8%8D%E5%8F%AF%E5%AE%9E%E4%BE%8B%E5%8C%96%E7%9A%84%E8%83%BD%E5%8A%9B%202286d0c7e726415198569a01b8f2cc0f.md)

[第5条：优先考虑依赖注入来引用资源](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC5%E6%9D%A1%EF%BC%9A%E4%BC%98%E5%85%88%E8%80%83%E8%99%91%E4%BE%9D%E8%B5%96%E6%B3%A8%E5%85%A5%E6%9D%A5%E5%BC%95%E7%94%A8%E8%B5%84%E6%BA%90%20de95e14a466047689e87e45b797d5825.md)

[第6条：避免创建不必要的对象](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC6%E6%9D%A1%EF%BC%9A%E9%81%BF%E5%85%8D%E5%88%9B%E5%BB%BA%E4%B8%8D%E5%BF%85%E8%A6%81%E7%9A%84%E5%AF%B9%E8%B1%A1%202943dc5f56cc4637a4f3a813cc7b7436.md)

[第7条：消除过期的对象引用](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC7%E6%9D%A1%EF%BC%9A%E6%B6%88%E9%99%A4%E8%BF%87%E6%9C%9F%E7%9A%84%E5%AF%B9%E8%B1%A1%E5%BC%95%E7%94%A8%20f535b371547742759a08bf9c37c07ca7.md)

[第8条：避免使用终结方法和清除方法](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC8%E6%9D%A1%EF%BC%9A%E9%81%BF%E5%85%8D%E4%BD%BF%E7%94%A8%E7%BB%88%E7%BB%93%E6%96%B9%E6%B3%95%E5%92%8C%E6%B8%85%E9%99%A4%E6%96%B9%E6%B3%95%2066926c6245e74d5c83f791402efce934.md)

[第9条：try-with-resources优先于try-finally](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC9%E6%9D%A1%EF%BC%9Atry-with-resources%E4%BC%98%E5%85%88%E4%BA%8Etry-finally%201f67f90fd0d340a8850f92cfe32c2a1c.md)

# 第三章：对于所有对象都通用的方法

尽管`Object`是一个具体类，但设计它的主要目的是为了扩展。它所有的非`final`方法(`equals、hashCode、toString、clone`和`finalize`)都有明确的通用约定，因为它们设计成是要被覆盖的。任何一个类，它在覆盖这些方法的时候，都有责任遵守这些通用的约定；如果不能做到这一点，其他依赖于这些约定的类（例如`HashMap`和`HashSet`）就无法结合该类一起正常的工作。

[第10条：覆盖equals时请遵守通用约定](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC10%E6%9D%A1%EF%BC%9A%E8%A6%86%E7%9B%96equals%E6%97%B6%E8%AF%B7%E9%81%B5%E5%AE%88%E9%80%9A%E7%94%A8%E7%BA%A6%E5%AE%9A%206e906e9de0fd4221889239620d68f22f.md)

[第11条：覆盖equals是总要覆盖hashCode](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC11%E6%9D%A1%EF%BC%9A%E8%A6%86%E7%9B%96equals%E6%98%AF%E6%80%BB%E8%A6%81%E8%A6%86%E7%9B%96hashCode%2072c34fff7cfa4660a3cf864740b69856.md)

[第12条：始终要覆盖toString方法](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC12%E6%9D%A1%EF%BC%9A%E5%A7%8B%E7%BB%88%E8%A6%81%E8%A6%86%E7%9B%96toString%E6%96%B9%E6%B3%95%20c33b777620384444ac34afd7cf98193e.md)

[第13条：谨慎的覆盖clone](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC13%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E7%9A%84%E8%A6%86%E7%9B%96clone%20b3f4a2a59483422ab57950daba8d82aa.md)

[第14条：考虑实现Comparable接口](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC14%E6%9D%A1%EF%BC%9A%E8%80%83%E8%99%91%E5%AE%9E%E7%8E%B0Comparable%E6%8E%A5%E5%8F%A3%20a8a88c2067834b0ebaa7a1b973168633.md)

# 第四章：类和接口

类和接口是Java编程语言的核心，它们也是Java语言的基本抽象单元。Java语言提供了许多强大的基本元素，供程序员用来设计类和接口。

[第15条：使类和成员的可访问性最小化](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC15%E6%9D%A1%EF%BC%9A%E4%BD%BF%E7%B1%BB%E5%92%8C%E6%88%90%E5%91%98%E7%9A%84%E5%8F%AF%E8%AE%BF%E9%97%AE%E6%80%A7%E6%9C%80%E5%B0%8F%E5%8C%96%208111135b6def43f1837a4ce49e10087d.md)

[第16条：要在共有类中使用访问方法而非公有域](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC16%E6%9D%A1%EF%BC%9A%E8%A6%81%E5%9C%A8%E5%85%B1%E6%9C%89%E7%B1%BB%E4%B8%AD%E4%BD%BF%E7%94%A8%E8%AE%BF%E9%97%AE%E6%96%B9%E6%B3%95%E8%80%8C%E9%9D%9E%E5%85%AC%E6%9C%89%E5%9F%9F%202f58f7b42eb74c47bc1cb66e71129e83.md)

[第17条：使可变性最小化](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC17%E6%9D%A1%EF%BC%9A%E4%BD%BF%E5%8F%AF%E5%8F%98%E6%80%A7%E6%9C%80%E5%B0%8F%E5%8C%96%2089e33bd553d44bf7998c6e4771fee9fb.md)

[第18条：复合优先于继承](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC18%E6%9D%A1%EF%BC%9A%E5%A4%8D%E5%90%88%E4%BC%98%E5%85%88%E4%BA%8E%E7%BB%A7%E6%89%BF%20906bac12f136433983e448c0d8050481.md)

[第19条：要么设计继承并提供文档说明，要么禁止继承](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC19%E6%9D%A1%EF%BC%9A%E8%A6%81%E4%B9%88%E8%AE%BE%E8%AE%A1%E7%BB%A7%E6%89%BF%E5%B9%B6%E6%8F%90%E4%BE%9B%E6%96%87%E6%A1%A3%E8%AF%B4%E6%98%8E%EF%BC%8C%E8%A6%81%E4%B9%88%E7%A6%81%E6%AD%A2%E7%BB%A7%E6%89%BF%2044ebcb5abfc3446e886df1d220e5154e.md)

[第20条：接口优于抽象类](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC20%E6%9D%A1%EF%BC%9A%E6%8E%A5%E5%8F%A3%E4%BC%98%E4%BA%8E%E6%8A%BD%E8%B1%A1%E7%B1%BB%20823ec0848b9f47ef87278cfe3ed72ac4.md)

[第21条：为后代设计接口](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC21%E6%9D%A1%EF%BC%9A%E4%B8%BA%E5%90%8E%E4%BB%A3%E8%AE%BE%E8%AE%A1%E6%8E%A5%E5%8F%A3%20d5efa8c7216948f58b67d75c5f9ef5a3.md)

[第22条：接口只用于定义类型](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC22%E6%9D%A1%EF%BC%9A%E6%8E%A5%E5%8F%A3%E5%8F%AA%E7%94%A8%E4%BA%8E%E5%AE%9A%E4%B9%89%E7%B1%BB%E5%9E%8B%200f8d30217da248d89e9483a4af4f3f3b.md)

[第23条：类层次优于标签类](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC23%E6%9D%A1%EF%BC%9A%E7%B1%BB%E5%B1%82%E6%AC%A1%E4%BC%98%E4%BA%8E%E6%A0%87%E7%AD%BE%E7%B1%BB%20c5b0615ad08b47c58008eb5f8489b9f6.md)

[第24条：静态成员优于非静态成员类](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC24%E6%9D%A1%EF%BC%9A%E9%9D%99%E6%80%81%E6%88%90%E5%91%98%E4%BC%98%E4%BA%8E%E9%9D%9E%E9%9D%99%E6%80%81%E6%88%90%E5%91%98%E7%B1%BB%20ae5cde541a434f9e9830c3be7b111039.md)

[第25条：限制源文件为当个顶级类](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC25%E6%9D%A1%EF%BC%9A%E9%99%90%E5%88%B6%E6%BA%90%E6%96%87%E4%BB%B6%E4%B8%BA%E5%BD%93%E4%B8%AA%E9%A1%B6%E7%BA%A7%E7%B1%BB%20deb766613c2148d9b4cb6c1d5df82aa7.md)

# 第五章：泛型

从Java 5开始，泛型已经成为了Java编程的一部分。在没有泛型之前，从集合中读取一个对象都必须进行转换。如果有人不小心插入了类型错误的对象，在运行时的转换处理就会出错。有了泛型之后，你可以告诉编译器每个集合中接受哪些对象类型。编译器自动为你的插入进行转换，并在编译时告知是否插入了类型错误的对象。

[第26条：请不要使用原生态类型](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC26%E6%9D%A1%EF%BC%9A%E8%AF%B7%E4%B8%8D%E8%A6%81%E4%BD%BF%E7%94%A8%E5%8E%9F%E7%94%9F%E6%80%81%E7%B1%BB%E5%9E%8B%201dac773d639c48d7b8e89809cc811128.md)

[第27条：消除非受检的警告](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC27%E6%9D%A1%EF%BC%9A%E6%B6%88%E9%99%A4%E9%9D%9E%E5%8F%97%E6%A3%80%E7%9A%84%E8%AD%A6%E5%91%8A%20a490a089d40a4fb68d31581d4d5ec3e7.md)

[第28条：列表优于数组](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC28%E6%9D%A1%EF%BC%9A%E5%88%97%E8%A1%A8%E4%BC%98%E4%BA%8E%E6%95%B0%E7%BB%84%20b93014e12ab24352b4b77a829be8bd25.md)

[第29条：优先考虑泛型](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC29%E6%9D%A1%EF%BC%9A%E4%BC%98%E5%85%88%E8%80%83%E8%99%91%E6%B3%9B%E5%9E%8B%20a350de2e21ba4ef6a2f83cb1525f39b6.md)

[第30条：优先考虑泛型方法](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC30%E6%9D%A1%EF%BC%9A%E4%BC%98%E5%85%88%E8%80%83%E8%99%91%E6%B3%9B%E5%9E%8B%E6%96%B9%E6%B3%95%2061c0304b5fdd4c3a8cd49c66b74a6a10.md)

[第31条：利用有限制通配符来提升API的灵活性](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC31%E6%9D%A1%EF%BC%9A%E5%88%A9%E7%94%A8%E6%9C%89%E9%99%90%E5%88%B6%E9%80%9A%E9%85%8D%E7%AC%A6%E6%9D%A5%E6%8F%90%E5%8D%87API%E7%9A%84%E7%81%B5%E6%B4%BB%E6%80%A7%203019339fc1c64339b4e8b5d3eab401be.md)

[第32条：谨慎并用泛型和可变参数](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC32%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E5%B9%B6%E7%94%A8%E6%B3%9B%E5%9E%8B%E5%92%8C%E5%8F%AF%E5%8F%98%E5%8F%82%E6%95%B0%20cdf4028420154e2ca9bf13c00ba6fabc.md)

[第33条：优先考虑类型安全的异构容器](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC33%E6%9D%A1%EF%BC%9A%E4%BC%98%E5%85%88%E8%80%83%E8%99%91%E7%B1%BB%E5%9E%8B%E5%AE%89%E5%85%A8%E7%9A%84%E5%BC%82%E6%9E%84%E5%AE%B9%E5%99%A8%2066d7ab5c0a7645ac8f25aaa2c7d858b2.md)

# 第六章：枚举和注解

Java支持两种特殊用途的引用类型：一种是类，称作枚举类型（enum type）；一种是接口，称作注解类型（annotation type）。

[第34条：用enum代替int常量](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC34%E6%9D%A1%EF%BC%9A%E7%94%A8enum%E4%BB%A3%E6%9B%BFint%E5%B8%B8%E9%87%8F%2031715e26df914a33a6d7e4eac17afb42.md)

[第35条：用实例域代替序数](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC35%E6%9D%A1%EF%BC%9A%E7%94%A8%E5%AE%9E%E4%BE%8B%E5%9F%9F%E4%BB%A3%E6%9B%BF%E5%BA%8F%E6%95%B0%20a0557a2543f4441a8823d6c35256d3de.md)

[第36条：用EnumSet代替位域](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC36%E6%9D%A1%EF%BC%9A%E7%94%A8EnumSet%E4%BB%A3%E6%9B%BF%E4%BD%8D%E5%9F%9F%200358f3f0bec24dff8107f9867ea60236.md)

[第37条：用EnumMap代替序数索引](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC37%E6%9D%A1%EF%BC%9A%E7%94%A8EnumMap%E4%BB%A3%E6%9B%BF%E5%BA%8F%E6%95%B0%E7%B4%A2%E5%BC%95%20b06a5801426749bf8fa6b20f7041d107.md)

[第38条：用接口模拟可扩展的枚举](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC38%E6%9D%A1%EF%BC%9A%E7%94%A8%E6%8E%A5%E5%8F%A3%E6%A8%A1%E6%8B%9F%E5%8F%AF%E6%89%A9%E5%B1%95%E7%9A%84%E6%9E%9A%E4%B8%BE%20421c6d1eec5048af8d58ad52d145dd4b.md)

[第39条：注解优先于命名模式](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC39%E6%9D%A1%EF%BC%9A%E6%B3%A8%E8%A7%A3%E4%BC%98%E5%85%88%E4%BA%8E%E5%91%BD%E5%90%8D%E6%A8%A1%E5%BC%8F%2042c2d9227d3148f88d1cfc9d8f5c08f1.md)

[第40条：坚持使用Overrride注解](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC40%E6%9D%A1%EF%BC%9A%E5%9D%9A%E6%8C%81%E4%BD%BF%E7%94%A8Overrride%E6%B3%A8%E8%A7%A3%207780d093f12b43a1857d092c0d805897.md)

[第41条：用标记接口定义类型](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC41%E6%9D%A1%EF%BC%9A%E7%94%A8%E6%A0%87%E8%AE%B0%E6%8E%A5%E5%8F%A3%E5%AE%9A%E4%B9%89%E7%B1%BB%E5%9E%8B%201f54f023a43144a989c817fa066fa908.md)

# 第七章：Lambda和Stream

在Java中，增加了函数接口（functional interface）、Lambda和方法引用（method reference），使得创建函数对象（function object）变得很容易。于此同时，还增加了Stream API，为处理数据元素的序列提供了类库基本的支持。

[第42条：Lambda优先于匿名类](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC42%E6%9D%A1%EF%BC%9ALambda%E4%BC%98%E5%85%88%E4%BA%8E%E5%8C%BF%E5%90%8D%E7%B1%BB%20779d715be0cf409baa713448b9e91745.md)

[第43条：方法引用优先于Lambda](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC43%E6%9D%A1%EF%BC%9A%E6%96%B9%E6%B3%95%E5%BC%95%E7%94%A8%E4%BC%98%E5%85%88%E4%BA%8ELambda%20c9ae83748d0a4785b9b3e06f119e406a.md)

[第44条：坚持使用标准的函数接口](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC44%E6%9D%A1%EF%BC%9A%E5%9D%9A%E6%8C%81%E4%BD%BF%E7%94%A8%E6%A0%87%E5%87%86%E7%9A%84%E5%87%BD%E6%95%B0%E6%8E%A5%E5%8F%A3%2028144d8edcf041ff9d1c05b1e8fcd3df.md)

[第45条：谨慎使用Stream](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC45%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E4%BD%BF%E7%94%A8Stream%205bda3b251f43403781b4bdf512e241c9.md)

[第46条：优先选择Stream中无副作用的函数](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC46%E6%9D%A1%EF%BC%9A%E4%BC%98%E5%85%88%E9%80%89%E6%8B%A9Stream%E4%B8%AD%E6%97%A0%E5%89%AF%E4%BD%9C%E7%94%A8%E7%9A%84%E5%87%BD%E6%95%B0%204e564c317fa74ff9befbfc0f98ebe0c8.md)

[第47条：Stream要优先用Collection作为返回类型](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC47%E6%9D%A1%EF%BC%9AStream%E8%A6%81%E4%BC%98%E5%85%88%E7%94%A8Collection%E4%BD%9C%E4%B8%BA%E8%BF%94%E5%9B%9E%E7%B1%BB%E5%9E%8B%2027aa79289957424ebda4bcd09a530d04.md)

[第48条：谨慎使用Stream并行](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC48%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E4%BD%BF%E7%94%A8Stream%E5%B9%B6%E8%A1%8C%206b5613e358f34b4784e43f758ba22b19.md)

# 第八章：方法

本章讨论方法设计的几个方面：如何处理参数和返回值，如何设计方法签名，如何为方法编写文档。

[第49条：检查参数的有效性](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC49%E6%9D%A1%EF%BC%9A%E6%A3%80%E6%9F%A5%E5%8F%82%E6%95%B0%E7%9A%84%E6%9C%89%E6%95%88%E6%80%A7%209dbcd9dbbe12444ba81a44b72fee28c1.md)

[第50条：必要时进行保护性拷贝](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC50%E6%9D%A1%EF%BC%9A%E5%BF%85%E8%A6%81%E6%97%B6%E8%BF%9B%E8%A1%8C%E4%BF%9D%E6%8A%A4%E6%80%A7%E6%8B%B7%E8%B4%9D%207f2da1c1fbf04277a8ded06749c60620.md)

[第51条：谨慎设计方法签名](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC51%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E8%AE%BE%E8%AE%A1%E6%96%B9%E6%B3%95%E7%AD%BE%E5%90%8D%20f07766a3efee459087addcbc014036a4.md)

[第52条：慎用重载](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC52%E6%9D%A1%EF%BC%9A%E6%85%8E%E7%94%A8%E9%87%8D%E8%BD%BD%20ccbad160a04945008403d1b3899a4da5.md)

[第53条：慎用可变参数](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC53%E6%9D%A1%EF%BC%9A%E6%85%8E%E7%94%A8%E5%8F%AF%E5%8F%98%E5%8F%82%E6%95%B0%2093af2d40641b4e43aa11403b0dc6dcf4.md)

[第54条：返回零长度的数组或者集合，而不是null](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC54%E6%9D%A1%EF%BC%9A%E8%BF%94%E5%9B%9E%E9%9B%B6%E9%95%BF%E5%BA%A6%E7%9A%84%E6%95%B0%E7%BB%84%E6%88%96%E8%80%85%E9%9B%86%E5%90%88%EF%BC%8C%E8%80%8C%E4%B8%8D%E6%98%AFnull%20582cc93f6d3341988bade4484d768caf.md)

[第55条：谨慎返回optional](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC55%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E8%BF%94%E5%9B%9Eoptional%204b9f26ae05424b8eb03944ea82a0ae5b.md)

[第56条：为所有导出的API元素编写文档注释](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC56%E6%9D%A1%EF%BC%9A%E4%B8%BA%E6%89%80%E6%9C%89%E5%AF%BC%E5%87%BA%E7%9A%84API%E5%85%83%E7%B4%A0%E7%BC%96%E5%86%99%E6%96%87%E6%A1%A3%E6%B3%A8%E9%87%8A%207658fe39512644929cbef154c0ae4010.md)

# 第九章：通用编程

本章主要讨论Java语言的细枝末节，包含局部变量的处理、控制结构、类库的用法、各种数据类型的用法，以及两种不是由语言本身提供的机制（反射机制和本地方法）的用法。最后讨论了优化和命名惯例。

[第57条：将局部变量的作用域做小化](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC57%E6%9D%A1%EF%BC%9A%E5%B0%86%E5%B1%80%E9%83%A8%E5%8F%98%E9%87%8F%E7%9A%84%E4%BD%9C%E7%94%A8%E5%9F%9F%E5%81%9A%E5%B0%8F%E5%8C%96%20f18d5cab81cc4288ba79a524e1410748.md)

[第58条：for-each循环优先于传统的for循环](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC58%E6%9D%A1%EF%BC%9Afor-each%E5%BE%AA%E7%8E%AF%E4%BC%98%E5%85%88%E4%BA%8E%E4%BC%A0%E7%BB%9F%E7%9A%84for%E5%BE%AA%E7%8E%AF%20f82c07ec4f6c43098fc51ef586834b45.md)

[第59条：了解和使用类库](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC59%E6%9D%A1%EF%BC%9A%E4%BA%86%E8%A7%A3%E5%92%8C%E4%BD%BF%E7%94%A8%E7%B1%BB%E5%BA%93%203e2fc8bbb13f4de6b08f3f582ac98be0.md)

[第60条：如果需要精确的答案，请避免使用float和double](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC60%E6%9D%A1%EF%BC%9A%E5%A6%82%E6%9E%9C%E9%9C%80%E8%A6%81%E7%B2%BE%E7%A1%AE%E7%9A%84%E7%AD%94%E6%A1%88%EF%BC%8C%E8%AF%B7%E9%81%BF%E5%85%8D%E4%BD%BF%E7%94%A8float%E5%92%8Cdouble%2093a435b13ea149dfbc725102e70a03d4.md)

[第61条：基本类型优先于装箱类型](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC61%E6%9D%A1%EF%BC%9A%E5%9F%BA%E6%9C%AC%E7%B1%BB%E5%9E%8B%E4%BC%98%E5%85%88%E4%BA%8E%E8%A3%85%E7%AE%B1%E7%B1%BB%E5%9E%8B%2004c0825c67084c738db33c04a1f33eed.md)

[第62条：如果其他类型更合适，则尽量避免使用字符串](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC62%E6%9D%A1%EF%BC%9A%E5%A6%82%E6%9E%9C%E5%85%B6%E4%BB%96%E7%B1%BB%E5%9E%8B%E6%9B%B4%E5%90%88%E9%80%82%EF%BC%8C%E5%88%99%E5%B0%BD%E9%87%8F%E9%81%BF%E5%85%8D%E4%BD%BF%E7%94%A8%E5%AD%97%E7%AC%A6%E4%B8%B2%2012eeb333549f4b6e8bedda2611d68d4b.md)

[第63条：了解字符串连接的性能](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC63%E6%9D%A1%EF%BC%9A%E4%BA%86%E8%A7%A3%E5%AD%97%E7%AC%A6%E4%B8%B2%E8%BF%9E%E6%8E%A5%E7%9A%84%E6%80%A7%E8%83%BD%20fce75aee75734041a4e82c4c4c0c3097.md)

[第64条：通过接口引用对象](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC64%E6%9D%A1%EF%BC%9A%E9%80%9A%E8%BF%87%E6%8E%A5%E5%8F%A3%E5%BC%95%E7%94%A8%E5%AF%B9%E8%B1%A1%2064f8c4959fcf42f2a840b128606e8934.md)

[第65条：接口优于反射机制](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC65%E6%9D%A1%EF%BC%9A%E6%8E%A5%E5%8F%A3%E4%BC%98%E4%BA%8E%E5%8F%8D%E5%B0%84%E6%9C%BA%E5%88%B6%20b378da6544bf4dbe97a6a422d2a79199.md)

[第66条：谨慎使用本地方法](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC66%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E4%BD%BF%E7%94%A8%E6%9C%AC%E5%9C%B0%E6%96%B9%E6%B3%95%20663f62aaa82a4dee93de5c837797a25c.md)

[第67条：谨慎地进行优化](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC67%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E5%9C%B0%E8%BF%9B%E8%A1%8C%E4%BC%98%E5%8C%96%201cdaf9d873e44a30a04503f8b5cdf406.md)

[第68条：遵守普遍接受的命名惯例](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC68%E6%9D%A1%EF%BC%9A%E9%81%B5%E5%AE%88%E6%99%AE%E9%81%8D%E6%8E%A5%E5%8F%97%E7%9A%84%E5%91%BD%E5%90%8D%E6%83%AF%E4%BE%8B%20868bd669a2ec424eb1cc6c642ade7709.md)

# 第十章：异常

充分发挥异常的优点，可以提高程序的可读性、可靠性和可维护性。如果使用不当，它们也会代理负面的影响。

[第69条：只针对异常的情况才是用异常](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC69%E6%9D%A1%EF%BC%9A%E5%8F%AA%E9%92%88%E5%AF%B9%E5%BC%82%E5%B8%B8%E7%9A%84%E6%83%85%E5%86%B5%E6%89%8D%E6%98%AF%E7%94%A8%E5%BC%82%E5%B8%B8%20c700c8ded4b7452a8b41e0b10c1826a9.md)

[第70条：对可恢复的情况使用受检异常，对编程错误使用运行时异常](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC70%E6%9D%A1%EF%BC%9A%E5%AF%B9%E5%8F%AF%E6%81%A2%E5%A4%8D%E7%9A%84%E6%83%85%E5%86%B5%E4%BD%BF%E7%94%A8%E5%8F%97%E6%A3%80%E5%BC%82%E5%B8%B8%EF%BC%8C%E5%AF%B9%E7%BC%96%E7%A8%8B%E9%94%99%E8%AF%AF%E4%BD%BF%E7%94%A8%E8%BF%90%E8%A1%8C%E6%97%B6%E5%BC%82%E5%B8%B8%20416e1e8ddeb345558b1f219e7b58dfdb.md)

[第71条：避免不必要地使用受检异常](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC71%E6%9D%A1%EF%BC%9A%E9%81%BF%E5%85%8D%E4%B8%8D%E5%BF%85%E8%A6%81%E5%9C%B0%E4%BD%BF%E7%94%A8%E5%8F%97%E6%A3%80%E5%BC%82%E5%B8%B8%2006bf5c571dee47c2bccd7421924b7239.md)

[第72条：优先使用标准的异常](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC72%E6%9D%A1%EF%BC%9A%E4%BC%98%E5%85%88%E4%BD%BF%E7%94%A8%E6%A0%87%E5%87%86%E7%9A%84%E5%BC%82%E5%B8%B8%20b79e609992bb45c9b416e1de59ba01b5.md)

[第73条：抛出抽象对应的异常](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC73%E6%9D%A1%EF%BC%9A%E6%8A%9B%E5%87%BA%E6%8A%BD%E8%B1%A1%E5%AF%B9%E5%BA%94%E7%9A%84%E5%BC%82%E5%B8%B8%20864594648ae84601b9c2bebbe4709800.md)

[第74条：每个方法抛出的所有异常都要建立文档](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC74%E6%9D%A1%EF%BC%9A%E6%AF%8F%E4%B8%AA%E6%96%B9%E6%B3%95%E6%8A%9B%E5%87%BA%E7%9A%84%E6%89%80%E6%9C%89%E5%BC%82%E5%B8%B8%E9%83%BD%E8%A6%81%E5%BB%BA%E7%AB%8B%E6%96%87%E6%A1%A3%200151eae2bc5a48dc937dbd1a5cdfc17a.md)

[第75条：在细节消息中包含失败-捕获信息](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC75%E6%9D%A1%EF%BC%9A%E5%9C%A8%E7%BB%86%E8%8A%82%E6%B6%88%E6%81%AF%E4%B8%AD%E5%8C%85%E5%90%AB%E5%A4%B1%E8%B4%A5-%E6%8D%95%E8%8E%B7%E4%BF%A1%E6%81%AF%2027ada2bdbe7f490abe81636a12ce7bd7.md)

[第76条：努力使失败保持原子性](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC76%E6%9D%A1%EF%BC%9A%E5%8A%AA%E5%8A%9B%E4%BD%BF%E5%A4%B1%E8%B4%A5%E4%BF%9D%E6%8C%81%E5%8E%9F%E5%AD%90%E6%80%A7%204be68e5ce0dc431e944e2ea16a7a611e.md)

[第77条：不要忽略异常](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC77%E6%9D%A1%EF%BC%9A%E4%B8%8D%E8%A6%81%E5%BF%BD%E7%95%A5%E5%BC%82%E5%B8%B8%209332408f98a8442396bb6709d4b850ba.md)

# 第十一章：并发

线程机制允许同时进行多个活动。并发程序设计比单线程程序设计要困难得多，因为有更多的东西可能出错，也很难重现失败。但是你无法避免并发，因为我们所做的大部分事情都需要并发，而且并发也是能否从多核的处理器中获得好的性能的一个条件，这些现在都是很平常的事了。本章阐述的建议可以帮助你编写出清晰、正确、文档组织良好的并发程序。

[第78条：同步访问共享的可变数据](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC78%E6%9D%A1%EF%BC%9A%E5%90%8C%E6%AD%A5%E8%AE%BF%E9%97%AE%E5%85%B1%E4%BA%AB%E7%9A%84%E5%8F%AF%E5%8F%98%E6%95%B0%E6%8D%AE%2042802fe8c4c44e78984339c060e50807.md)

[第79条：避免过度同步](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC79%E6%9D%A1%EF%BC%9A%E9%81%BF%E5%85%8D%E8%BF%87%E5%BA%A6%E5%90%8C%E6%AD%A5%20210266974dde4fb284ae2ae95c36afda.md)

[第80条：executor、task和stream优先于线程](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC80%E6%9D%A1%EF%BC%9Aexecutor%E3%80%81task%E5%92%8Cstream%E4%BC%98%E5%85%88%E4%BA%8E%E7%BA%BF%E7%A8%8B%20ce77207a451d442ca6623f11c3795dc6.md)

[第81条：并发工具优先于wait和notify](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC81%E6%9D%A1%EF%BC%9A%E5%B9%B6%E5%8F%91%E5%B7%A5%E5%85%B7%E4%BC%98%E5%85%88%E4%BA%8Ewait%E5%92%8Cnotify%2021141bf16fbe4ff7b1499c946bd96b41.md)

[第82条：线程安全性的文档](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC82%E6%9D%A1%EF%BC%9A%E7%BA%BF%E7%A8%8B%E5%AE%89%E5%85%A8%E6%80%A7%E7%9A%84%E6%96%87%E6%A1%A3%203ee8f387c10146329231940c0d0f35de.md)

[第82条：线程安全性文档](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC82%E6%9D%A1%EF%BC%9A%E7%BA%BF%E7%A8%8B%E5%AE%89%E5%85%A8%E6%80%A7%E6%96%87%E6%A1%A3%2034a00c697f434eb3bb003f75a39d491c.md)

[第83条：慎用延迟初始化](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC83%E6%9D%A1%EF%BC%9A%E6%85%8E%E7%94%A8%E5%BB%B6%E8%BF%9F%E5%88%9D%E5%A7%8B%E5%8C%96%20d8a70fa30b4348d098f10e04fea4ee44.md)

[第84条：不要依赖线程调度器](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC84%E6%9D%A1%EF%BC%9A%E4%B8%8D%E8%A6%81%E4%BE%9D%E8%B5%96%E7%BA%BF%E7%A8%8B%E8%B0%83%E5%BA%A6%E5%99%A8%20173dc36ea99048f5948b0a63aaff6ddf.md)

# 第十二章：序列化

本章讨论对象序列化（object serialization），它是Java的一个框架，用来将对象编码成字节流（序列化），并从字节流编码中重新构建对象（反序列化）。一旦对象序列化之后 ，它的编码就可以从一台正在运行的虚拟机被传到另一台虚拟机上，或者被存储到磁盘上，供后续反序列化时使用。本章主要关注序列化的风险，以及如何将风险降到最低。

[第85条：其他方法优先于Java序列化](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC85%E6%9D%A1%EF%BC%9A%E5%85%B6%E4%BB%96%E6%96%B9%E6%B3%95%E4%BC%98%E5%85%88%E4%BA%8EJava%E5%BA%8F%E5%88%97%E5%8C%96%204debf4b3b71c42e3a5924abd63a5e28e.md)

[第86条：谨慎地使用Serializable接口](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC86%E6%9D%A1%EF%BC%9A%E8%B0%A8%E6%85%8E%E5%9C%B0%E4%BD%BF%E7%94%A8Serializable%E6%8E%A5%E5%8F%A3%20e8f055a4c1b74216a4ae50614d2d903d.md)

[第87条：考虑使用自定义的序列化形式](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC87%E6%9D%A1%EF%BC%9A%E8%80%83%E8%99%91%E4%BD%BF%E7%94%A8%E8%87%AA%E5%AE%9A%E4%B9%89%E7%9A%84%E5%BA%8F%E5%88%97%E5%8C%96%E5%BD%A2%E5%BC%8F%20b40ef181101d4e7b9414480999f04c31.md)

[第88条：保护性地编写readObject方法](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC88%E6%9D%A1%EF%BC%9A%E4%BF%9D%E6%8A%A4%E6%80%A7%E5%9C%B0%E7%BC%96%E5%86%99readObject%E6%96%B9%E6%B3%95%2090677849b4a141ef8bd848fd5d406d19.md)

[第89条：对于实例受控制，枚举类型优先于readResolve](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC89%E6%9D%A1%EF%BC%9A%E5%AF%B9%E4%BA%8E%E5%AE%9E%E4%BE%8B%E5%8F%97%E6%8E%A7%E5%88%B6%EF%BC%8C%E6%9E%9A%E4%B8%BE%E7%B1%BB%E5%9E%8B%E4%BC%98%E5%85%88%E4%BA%8EreadResolve%20ca05d3177186481cbf40e66493903c2a.md)

[第90条：考虑用序列化代理代替序列化实例](%E3%80%8AEffective%20Java%E3%80%8B%206455c255249a4f85af5589bed107db16/%E7%AC%AC90%E6%9D%A1%EF%BC%9A%E8%80%83%E8%99%91%E7%94%A8%E5%BA%8F%E5%88%97%E5%8C%96%E4%BB%A3%E7%90%86%E4%BB%A3%E6%9B%BF%E5%BA%8F%E5%88%97%E5%8C%96%E5%AE%9E%E4%BE%8B%208f54f900213a48aab633441ff5590046.md)