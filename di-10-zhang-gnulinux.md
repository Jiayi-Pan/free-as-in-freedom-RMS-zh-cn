# 第10章 GNU/Linux

1993年，自由软件运动的发展到了一个转折点。从乐观的角度讲，种种迹象都表明黑客文化正在变得越来越成功。《连线》杂志作为一本新兴的时尚杂志，用有关数据加密、新闻组、自由软件等热门话题在读者面前树立了自己的品牌形象。而Internet这个原本只在黑客和科学家群体中流行的词汇，也渐渐地融入了主流社会，就连时任美国总统的克林顿也不忘提到它。昔日作为数码爱好者玩具的个人电脑，得到了广泛的普及。同时，黑客们所开发的软件也进入了新一代计算机用户的视野。然而，GNU工程却还没完成它创建一个完整自由操作系统的目标，喜欢尝鲜的用户只能使用Linux作为一个替代系统。

不管你怎么想，这听起来仍然是个好消息，或者至少看起来是。经过了十年的挣扎，黑客和黑客的价值观终于开始被主流社会所接受，大众开始接纳这种文化。

事实确实如此吗？从悲观的角度来说，被大众所接受也就意味着麻烦正在滋长。成为一个黑客突然变成了一件很酷的事情，但是对于一个社区而言，这种疏远大众的繁荣真的算是一件好事吗？当然，白宫表明态度说Internet是一个很好的趋势，甚至已经在网上注册了自己的域名：whitehouse.gov，但是它也在召集各个公司、审查机关和执法机构一同开会，设法管理如同西部荒原般的Internet文化。是的，个人电脑正在变得越来越强大，但是Intel作为个人计算机市场上的芯片供应商，已经帮助软件公司一起，形成了一种由专有软件开发商垄断的局面。虽然有很多人通过Linux接触并开始使用自由软件，但与此同时，有成百上千的人成为了微软Windows的用户。

到头来，这是Linux奇妙的天性。它没有像GNU那样的设计错误，也没有BSD那样的法律争论，Linux的高速发展完全是出乎意料的，它的成功也是偶然的，甚至于编写了它的代码的程序员们也没法想象事情为什么会发展成这样。Linux比一个完整的操作系统更为复杂，它完全就是一个黑客们把各种顶级工具混杂在一起的产物：从GCC、GDB和glibc（GNU工程新开发的C库）到X（麻省理工学院的计算机科学实验室开发的基于Unix架构的图形化用户界面），还包括BSD开发的那些类似于BIND（the Berkeley Internet Naming Daemon，用于提供把IP地址与域名进行映射的网络服务）和TCP/IP协议。整个体系最为精华的部分，当然就是Linux内核本身，它是一个在Minix基础上重新开发的全新的内核。托瓦兹和他高速成长的Linux开发团队并没有把所有东西都从头造一遍，而是遵循了古老的毕加索的格言：“能工摹其形，巧匠摄其魂。”后来，托瓦兹本人也以类似的说法评价他自己成功的秘诀：“我是一个非常懒惰的人，并且喜欢把别人的成果占为已有\[1]。”

这种所谓的惰性，从提高效率的角度来看，还是非常值得景仰的，但是从政治的角度来看就变得很棘手。从中可以看出，托瓦兹对于整件事并没有一个理智的规划。与GNU开发者不同，托瓦兹从一开始就没有想过要让他的团队一起来开发一个完整的操作系统，他只是想做一个自己可以玩的东西。就像汤姆・索亚粉刷篱笆一样，托瓦兹的天才能力并不表现在他的大局观上，而是在于他可以召集到一批黑客一起努力，用最快的速度完成任务。

托瓦兹和他找来一同工作的黑客们大获成功，而其他人则产生了一些疑问：那么，准确来说，Linux究竟是个什么东西呢？它是不是对斯托曼在GNU宣言中所表述的自由软件哲学的一种表现形式呢？还是只是一个人们在家用电脑上就可以土法炮制出来的简单的工具集合呢？

到了1993年下半年，越来越多的Linux用户开始倾向于后一种定义并开始基于Linux开发各种变种。他们甚至开始把这些衍生版本（或者说“发行版”）包装起来并向Unix爱好者出售，但这些版本的质量可谓是参差不齐。

“这就是红帽公司（Red Hat）或其他商业发行版出现前的情况。”伊恩・默多克（Ian Murdock）回忆道，那时他还是普渡大学计算机系的一名学生。“如果你翻阅Unix的杂志，你会看到很多名片大小的小广告推广‘Linux’。这些公司有很多会在自己的发行版里添加些自己的程序和代码。然而，这些公司往往只干几年就销声匿迹了。”

作为一名Unix程序员，默多克还记得他第一次在家里的个人电脑上下载安装Linux时，被这个系统“扫地出门”的情景。“不过这仍是一件充满乐趣的事情，”他说，“这让我感觉到自己参与到了这个项目中。”然而，各种低质发行版的泛滥渐渐消耗了他的早期的热情。默多克认为，参与到这个项目中的最好的的方式就是开发一个不添加任何额外组件的Linux发行版。于是，他开始收集各种最好的自由软件工具，打算把它们整合到他自己的发行版中。默多克说：“我希望能创造出一个对得起Linux这个名字的系统。”

为了“激发人们的兴趣”，默多克在包括comp.os.linux这个Usenet新闻组在内的各种网上渠道发布了他的想法。最早回复他的电子邮件中有一封来自rms@ai.mit.edu。作为一个黑客，默多克立刻就认出了这个邮件地址。这就是理查德・斯托曼，GNU工程的创始人，一个在默多克心目中被认为是“黑客中的黑客”的传奇人物。在邮件地址列表中看到他的邮件地址，默多克感到有点疑惑。为什么斯托曼这个正在引领自己的操作系统工程的人物，会关心默多克对Linux所发的牢骚？

默多克打开了这封邮件。

“他说自由软件基金会正在开始进一步关注Linux，并很有兴趣基于Linux来完成一个操作系统。也就是说，好像斯托曼对我们所想做的事很有兴趣，这和他们努力的方向是一致的。”

这封信展现了斯托曼立场的360度大转弯。在1993年之前，斯托曼一直都不干涉Linux社区的事务。事实上，当Linux在1991年开始出现在Unix编程的范畴中开始，他都还是回避这个操作系统。斯托曼说，当他得知有一个可以在PC平台上运行的类Unix系统时，他找了一个朋友帮忙去了解这个系统的相关情况。“他汇报说这个系统是以System V作为原型的，这是一个比较低劣的Unix版本。并且，他告诉我，这个系统是不可移植的。”

斯托曼朋友的报告并不完全正确。Linux是为基于386的机器所设计的，这就意味着Linux生根于这类低成本的平台。他的朋友没有发现Linux所内涵的一个重大优势，那就是它是当时市面上唯一个可以自由修改的操作系统。换句话说，在接下来的三年时间中，当斯托曼还在听取Hurd团队的Bug报告时，托瓦兹正在赢得广大程序员的支持，他们成为把Linux移植到各种新的硬件平台的中坚力量。

直到1993年，GNU工程还是没能发布一个可以使用的操作系统内核，这对GNU工程甚至于自由软件运动本身都产生了不小的影响。1993年3月，西姆森・加芬克尔在《连线》杂志上发表了一篇文章，把GNU工程描述为一个“深陷泥沼”的项目，全然无视这个项目中所创造出来的那些成功的工具\[2]。GNU工程的成员，以及GNU工程的非营利性赞助商——自由软件基金会的一些成员回忆说，当时的大家的心情非常不好，甚至加芬克尔的文章对大家造成的伤害都已经显得不是那么重要了，“当时的情况很明显，至少在我看来是这样，那就是引入一个全新的操作系统需要一个时间窗口，”查瑟尔说，“一旦错过了这个时间窗口，人们对新的系统就不会有太大的兴趣，但这却正是当时大家所面临的情况\[3]。”

1990年～1993年期间，GNU工程一直处在挣扎中。有些人为此批评斯托曼，但GNU Emacs早期团队中的一员并后来成为斯托曼批评家的埃里克・雷蒙德认为，造成一切问题的根源是体制。“自由软件基金会太骄傲了，”雷蒙德说，“他们把自己的目标从开发一个成熟的操作系统，转移到了进行操作系统的研究。他们认为除了自由软件基金会，没人可以对他们造成影响。”

默多克，作为一名并不参与GNU工程内部运作的人，更具有包容的观点。“我认为问题的一方面是他们有点过于好高骛远，把钱投入了不正确的地方，”默多克说道，“微内核在80年代和90年代初期是一个非常热门的话题。很不幸的是，那正是GNU工程开始设计他们的内核的时间，结果就是带来了很多额外的包袱，这些包袱很难被轻易甩掉。”

斯托曼自己则寻找了一些客观因素来解释整个项目延期的原因。莲花和苹果的官司带来了政治上的分心，加上那时斯托曼手上的病症，导致他不能全身心地投入到Hurd的团队中去。斯托曼还说，GNU工程中各个部分之间缺乏有效的沟通。“我们花了很多时间才使调试环境可以正常工作起来，”他回忆道，“而那时维护GDB的团队又并不是很合作。”但是，斯托曼也说，他和其他GNU工程的成员低估了把Mach微内核扩展成为一个完整的Unix内核的难度。

“我以为Mach内核中与硬件通信的部分已经调试无误了，”斯托曼在2000年一次演讲中回忆Hurd团队遇到的问题时说，“如果有这个为基础，我们的进展会更为顺利一些。但是，事实上调试这些异步运行的多线程程序非常困难。一些时序处理上的小小问题就会导致文件损坏，这一点也不好玩。最终的结果就是，我们花了很多年的时间，还是只能开发出一个测试用的版本\[4]。”

不管是一个借口还是一堆借口，当时的情况就是Linux内核的成功给GNU工程造成了一种紧张的气氛。毫无疑问，Linux内核确实已经按GPL发布，但正如默多克自己所发现的那样，想要把Linux当成是一个纯自由软件操作系统还有很长的路要走。截至1993年年底，Linux的总用户数已经从数十名Minix爱好者发展到20000～100000人\[5]。曾经的个人爱好已经成长为一个快速发展的市场。就像温斯顿・丘吉尔（Winston Churchill）看到苏联军队攻入柏林的感觉一样，看到Linux的“胜利”，斯托曼心里像是打翻了五味瓶\[6]。

虽说是赶了个晚集，但斯托曼还是有着巨大的影响力。当自由软件基金会宣布它会向默多克的软件项目提供资金和精神支持时，其他各方面的支持也开始源源不断的涌入。于是，默多克启动了一个名为Debian的新项目，这个项目的名字是用他和他夫人黛博拉（Deborah）的名字构成的。在短短的几个星期后，这个项目就发布了第一个版本。“理查德的帮助使得这个出于个人兴趣开发的小小的项目在一夜间变成了社区中每一个人都很关注的明星项目。”默多克说。

1994年1月，默多克发布了“Debian宣言”，这个宣言与斯托曼十年前发布的“GNU宣言”在精神上非常一致，它解释了Debian与自由软件基金会紧密合作的重要性。默多克写道：

自由软件基金会对于Debian的未来具有非常重要的意义。他们可以帮助分发Debian，向全世界发出信号，Linux不是也不应该是一个商业化的产品，但这并不意味着 Linux就比不上商业产品。如果你们有人不同意这个观点，我可以用GNU Emacs和GCC的例子来证明，它们都不是商业软件，但它们都对商业市场产生了重大的影响。

已经到了集中精力关注Linux未来的时候了，不应该以Linux 社区毁灭和它未来的消亡作为代价来实现个人富裕的目标。虽然开发和发布Debian也许并不能回答我在宣言中提出的问题，但我希望它至少可以帮助大家更多关注这些问题并一起想办法解决它们\[7]。

宣言发布后不久，自由软件基金会就向Debian提出了一个要求。斯托曼希望默多克把他的发行版叫作“GNU/Linux”。默多克说，刚开始的时候，斯托曼曾希望他们使用“Lignux”这个名字，表示GNU是Linux系统的心脏。但是这个名字在Usenet和一些即席的黑客团体的调查中得到的嘘声迫使斯托曼退而求其次，改用GNU/Linux这个相对自然一点的名字。

斯托曼想过GNU前缀的方式去强调GNU在Linux系统中所发挥的重要作用，很多人也许根本就不会注意到这一点，默多克的观点则不尽相同。在那个时候，默多克把这个看成是消除GNU工程和Linux内核开发者之间紧张关系的一种尝试。默多克回忆说，“那时候两个社区之间出现了一些分裂，理查德对此非常重视。”

默多克认为最大的隔阂出现在glibc上。glibc是GNU C库的缩写，用于让程序员可以直接调用操作系统内核所提供的“系统调用”。1993年～1994年间，glibc一度是Linux开发过程中最大的瓶颈。由于很多的Linux用户不断地向Linux内核添加系统调用，GNU工程的glibc的维护人员很快就被各种需求压得喘不过气来。由于GNU工程不断地延期，给人们留下了拖后腿的印象，有些Linux开发者提出要给glibc创建一个Linux专用的分支。

在黑客的世界中，分支是一个很有意思的现象。虽然黑客的行为道德中允许一个程序员对程序的代码做任何的改进，但是大部分黑客都希望自己的改动能进入程序源代码的主干中，这样才能保证与其他人的程序保持最大程度上的兼容。如果在Linux开发的初期就对glibc创建分支，那就意味着可能会失去成百上千的Linux开发者。这也会造成Linux与斯托曼和GNU团队期望开发出的GNU系统之间的不兼容。

作为GNU工程的领导者，斯托曼早在1991年时就认识到了创建软件分支的不良后果了。那时候，有一批就职于Lucid公司的Emacs开发人员与斯托曼闹翻了，因为斯托曼不原意把他们对Emacs代码修改合入Emacs代码主干，于是，他们不得不创建了一个名为Lucid Emacs的分支版本\[8]。

默多克说，当时Debian也是出于类似原因才对glibc创建了一个分支版本，这导致斯托曼坚持要在发布Debian发行版时加上GNU前缀。“这个分支最终还是逐渐与主干合并。然而，在那个时候，人们还是很担心Linux社区是否会把自己与GNU社区割裂开来，这样做会造成开发力量分散。”

斯托曼赞同默多克的看法。事实上，大部分主要的GNU组件在刚开始的时候都有多个分支版本。起初，斯托曼认为这些分支就像酸葡萄。与Linux内核开发组快速和作坊式的开发模式不同，GNU的源代码维护者更倾向于用一种更慢更谨慎的方式去开发程序，以保证程序长期的活力。他们对于批评其他人的代码也毫不吝啬。然而，时间慢慢流逝，斯托曼在阅读Linux开发者的电子邮件时候，发觉到他们缺乏对GNU工程和它的目标的基本认识。

斯托曼说：“我们发现那些认为自己是Linux用户的人们并不关心GNU工程。他们说，‘为什么我们要花力气去做这些事？我不关心GNU工程。我只关心Linux可以正常运行，其他都与我无关。’这样的想法很让人吃惊，因为他们事实上正在使用着GNU系统的一个变种，而他们甚至比其他人更容易忽略这个事实。”

虽然有不少人觉得把Linux看成是GNU工程的一个“变种”在政治上未免显得有点贪心，默多克却对自由软件情有独钟，他觉得斯托曼要求把Debian称为GNU/Linux是合理的。“团结开发者比争抢名号更为重要。”默多克表示。

默多克很快建议，减少政治上的讨论，把更多精力集中到技术上来。虽然默多克对讨论政治问题已经习以为常，但说起设计和开发软件，他一定会坚持己见。这股默多克带来的风气很快蔓延到了别的GNU项目中。

默多克笑着说：“我可以告诉你，在很多方面我与斯托曼的看法都不一致。实事求是地说，理查德是一个很难与之合作的人。”

1996年，默多克从普渡大学毕业后，打算找人接手正在蓬勃发展的Debian项目。那时候，他已经把主要的管理职责都转交给了布鲁斯・佩伦斯，佩伦斯是Unix下的知名软件Electric Fence的作者，这个软件也使用GPL许可证来发布。佩伦斯与默多克一样，在GNU/Linux刚刚展现出与Unix的巨大相似性时，就喜欢上了它。他也和默多克一样，虽然没有与斯托曼和自由软件基金会有过实际的接触，但他对他们的政治目标抱有极大的兴趣。

“我记得斯托曼设计出了《GNU宣言》、GNU Emacs和GCC后，有篇文章说他正在为Intel提供咨询服务，”佩伦斯回忆起他在80年代末期第一次与斯托曼接触的情景，说道，“我写信给他，问他是怎么做到一方面宣扬自由软件又一方面为Intel工作的。他回信说：我是作为Intel开发自由软件的咨询师身份为他们工作的。他的回答很有礼貌，而且也很有道理。”

然而，作为一个杰出的Debian开发者，佩伦斯对于默多克和斯托曼之间的矛盾感到遗憾。作为开发团队的领导者，佩伦斯说他决定让Debian与自由软件基金会保持距离。他说：“我决定不采用理查德风格的微管理模式。”

佩伦斯表示，斯托曼对这样的决定大吃一惊，但他仍然有能力去驾驭这样的复杂局面。“他给了我们一些时间冷静下来，然后发了一个邮件说我们需要建立一种合作关系。他要求我们把这个系统叫作GNU/Linux，并一直这样称呼它。我个人觉得这样是可以的。我单方面做出了决定，采纳了这个名字，让每个人都舒了一口气。”

在很长的一段时间里，Debian都被看成是最适合黑客们的Linux发行版之一，在1993年～1994年这段时间，Slackware也是一个非常流行的发行版。虽然Linux不是一个真正意义上面向黑客的系统，但是Linux在商业Unix的市场中也找到了自己的位置。在北卡罗来纳州，一个名叫红帽的Unix公司，把他们的注意力慢慢转向了Linux。红帽公司的首席执行官是罗伯特・杨，他曾经是Linux通讯杂志的编辑，并在1994年时采访过林纳斯・托瓦兹，问他对于把内核以GPL来发布是否后悔。对于杨来说，托瓦兹的回答让他对Linux有了进一步深层次的认识，他不再寻求通过传统软件销售策略的方式把GNU/Linux边缘化，而是开始思考如果一家公司像Debian那样思考问题，会出现什么情况。比如，发布一个完全由自由软件构成的操作系统。1990年，迈克尔・蒂曼和约翰・吉尔摩成立的Cygnus Solutions的公司，早已经向世人证明通过销售自由软件相关的定制化服务是可以盈利的。如果红帽公司对于GNU/Linux采用类似的策略会如何？

“在西方的科学传统上，我们需要站在巨人的肩膀上（指的是托瓦兹和艾萨克・牛顿（Isaac Newton）爵士），”杨说，“在商业上，这就告诫我们，应该在前进的途中避免重新造轮子。GPL模式的美在于把你的代码放入公有领域\[9]。如果你是一个独立软件提供商并且想开发一个软件，比如你需要开发一个调制解调器拨号程序，但是你没有必要重新开发一个拨号程序。你可以直接从Red Hat Linux中‘盗取’PPP的实现，并把它作为你的拨号程序的核心。如果你需要一个图形工具集，你不需要重新去实现一个你自己的图形库。你只需要下载GTK，就可以立刻使用前人的成熟的果实。于是，你就可以专心做你的软件提供商，少花一点时间在软件管理上，而多花一些时间在你客户所想要的功能上。”

杨并不是唯一一个从自由软件的高效性中受到启发的CEO。1996年年末，大部分Unix公司开始清醒过来，并嗅到了源代码的香味。那时候，Linux距离成为一个完整的商用操作系统还有一两年的路要走，但是黑客社区还是感觉到这一天已经离得很近了：一场巨大的变革即将到来。Intel 386芯片、Internet和万维网像一波外星人入侵一样深入地影响了整个市场，而Linux这个可以自由使用其源代码并以宽松的许可证发布的程序包，则是这一波外星人中最强大的一个。

对于试图讨好斯托曼但后来又厌恶斯托曼的微管理风格的伊恩・默多克来说，他在自由软件运动中花费了很多的精力，这波变革看上去既是对他的赞美又是对他的惩罚。与很多Linux发烧友一样，默多克看到过托瓦兹最初的那个帖子，他看到过托瓦兹最初把Linux看作是“兴趣爱好”的想法。他也看到了托瓦兹在回复Minix作者安德鲁・塔嫩鲍姆的帖子中坦言：“如果GNU内核在去年春天时就已经完成，我就不会再启动我自己的这个项目\[10]。”像很多人一样，默多克知道，这种好机会已经错过了。他也看到了Internet即将带来的巨大的机遇。

“在早期参与到Linux项目中充满着乐趣，”默多克回忆道，“在同一段时间里，有些东西在向前进步，有些东西则成为过眼烟云。如果你回头去看看comp.os.minix上的那些老帖子，你会看到这样的观点——这是在Hurd开发完成前我们可以先玩着的东西。人们总是性急的。它很好玩，但是如果Hurd来得更早一些的话，我想Linux可能就根本不会出现。”

到了1996年年底，所有这些“如果”都已经盖棺定论。不管是称呼它为Linux或是GNU/Linux，用户们已经用行动证明了Linux的成功。36个月的时间窗口已经关闭，意味着即使GNU工程可以开发出Hurd内核，除了GNU的核心黑客们以外也不会有更多人会注意它。第一个类Unix的自由软件操作系统就在每个人的眼前，并且充满活力。黑客们所要做的就是安静地坐下来，等待下一波新的想法出现在他们的头脑中。即使是长着蓬乱的头发的理查德・斯托曼本人也不例外。

准备好出发了吗？

注　释

\[1].托瓦兹在很多场合都引用过这个说法。到目前为止，最确切的一次是在埃里克・雷蒙德的文章《大教堂与集市》中出现的（1997年5月）。http://www.tuxedo.org/～esr/writings/cathedral-bazaar/cathedral-bazaar/index.html。

\[2].参考辛姆森・加芬克尔的文章，“斯托曼深陷泥沼？”，《连线》杂志，1993年3月。

\[3].查瑟尔所说的对于一个新的操作系统来说有36个月的“时间窗口”的理论，并不仅仅适用于GNU工程。在20世纪90年代初，BSD的自由版本由于他们与Unix系统实验室之间的官司，导致迟迟不能发布。虽然很多人认为BSD比GNU/Linux性能更好、更稳定，并坚持使用FreeBSD或OpenBSD，但是跟使用GNU/Linux的人数相比，这依然只是一个很小的数字。

\[4].参考斯托曼在茂宜高性能计算中心的演讲。

\[5].很难准确统计出GNU/Linux的用户数，所以我在这里只是提供了一个非常宽泛的估计值。100000这个数字来源于红帽公司的“里程碑”网站，http://www.redhat.com/about/corporate/milestones.html。

\[6].用丘吉尔跟斯托曼作类比，是我个人的想法。后来斯托曼向我表达了他对丘吉尔的评价：第二次世界大战在是我成长经历中一段不能抹去的记忆。就像丘吉尔所说的：“我们要与敌人在登陆地点作战，我们要与敌人在沙滩作战……我们决不投降！”这句话一直都能引起我的共鸣。

\[7].参考伊恩・默多克的《Debian简明发展史》，1994年1月6日：附录 A，“Debian宣言”，http://www.debian.org/doc/manuals/project-history/apA.html。

\[8].杰米・泽文斯基（Jamie Zawinski）是Mozilla开发团队的一员，他曾经是Lucid公司的程序员，他维护了一个记录Lucid/GNU Emacs分支的网站，名为“The Lemacs/FSFmacs Schism”。http://www.jwz.org/doc/lemacs.html。

\[9].杨在这里错误的使用了“公有领域”一词，公有领域就意味着不受版权保护。但使用GPL许可证的软件从根本就上保证了是受版权保护的。

\[10].这句话引自在Linux刚刚发布以后，托瓦兹与塔嫩鲍姆之间一场有名的争论。托瓦兹为他选择移植性较差的单一内核的设计进行辩护，他说这样做是因为他想更深入的研究他的386电脑。“如果GNU内核在去年春天时就已经完成，我就不会再启动我自己的这个项目。”参考克里斯・迪邦纳（Chris DiBona）等著的《开源软件文集》一书，O'Reilly & Associates,Inc.，1999年，第24页。
