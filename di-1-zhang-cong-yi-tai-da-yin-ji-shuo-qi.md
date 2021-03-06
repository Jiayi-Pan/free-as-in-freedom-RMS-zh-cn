# 第1章 从一台打印机说起

我畏惧希腊人，哪怕他们带着礼物来。

——维吉尔，《埃涅阿斯纪》

这可是台全新的打印机！怎么又卡纸了？

理查德・M・斯托曼（Richard M. Stallman）刚刚发现了这问题，这可苦了他了。他当年27岁，是麻省理工学院人工智能实验室的一名程序员。一个小时前，他给那台激光打印机提交了一个50页的打印任务，之后就忙着干活去了。现在他正站在那台打印机前面，眼巴巴地看着它被纸卡住：总共才打印了的四页纸，还没有一页是自己的。换句话说，斯托曼那份50页的文件，外加别人的半份文档，全被一张纸卡住了，成了实验室网络上的两个孤魂野鬼。

干程序员这行也是有风险的：你总得等着机器干活。不过斯托曼还是能苦中作乐。可再怎么说，等着机器干活，和在它跟前盯着它干活毕竟是两码事。就说现在吧，斯托曼正盯着打印机，看它一页一页慢吞吞地往外吐纸。这情景对他来说可不陌生。斯托曼好歹也是个程序员，成天都在改进机器和程序，提高它们的效率。当下，他恨不得掀开这台打印机，仔细查查究竟是哪里出的毛病。

可惜，凭编程的能耐，没法解决机械工程的问题。斯托曼只能在重新打印文件的这些时间想点别的：能不能用别的办法，绕道解决这个卡纸的问题？

这台打印机来人工智能实验室有多久了？斯托曼努力回忆着。这机器是施乐公司（Xerox Corporation）捐赠的。它可是新一代产品的原型，是从上一代的复印机改进而来。和上一代比，它不再是简单地复印文件，而是从网络上接收数据，打印成专业品质的文档。它诞生于著名的施乐帕罗奥多研究中心（Xerox Palo Alto Research Facility）。再过大约十年，将会发生一场打印机革命，那时，许多计算机厂商都会投身其中。而这款打印机则是这场革命的先行者。

人工智能实验室的程序员们，本能般地喜欢折腾这些新酷产品。当初他们麻利地把这打印机请回来，把它和实验室中的各种复杂的计算设备连在了一起，结果甚是喜人。比起以前的打印机，这台新打印机打印速度飞快。平均大约一秒打印一页纸。以前要花二十多分钟打印的东西，如今两分钟就解决了。新机器的打印精度也更高了。让它给画个圆，它绝不会打出个鸡蛋；让它画条直线，它也绝不会拐着弯瞎划拉。

怎么看，这打印机都是份难以拒绝的礼物。

可没过几周，这机器的缺点就逐渐显现了。其中最要命的，就是卡纸问题。凭着工程师的直觉，程序员们很快就洞察出了这问题背后的诱因。这台打印机是在复印机的基础上设计的。倘若是一台复印机，它旁边总会站个人直接操作它。遇到卡纸问题，这个人总能立即发现，着手解决，不至于有什么大影响。用工程师的行话讲，这系统需要用户参与。所以，对于复印机来说，卡纸问题也就没人关注了。设计复印机的时候，施乐公司的工程师们都没把卡纸的事情放在心上，专心去对付其他问题了。可把类似的机械部件用在打印机上，问题就来了。

施乐公司在复印机的基础之上，设计了这个打印机。这个小小的变化，却使得人机关系发生了微妙而深刻的改变。现在，在同一时刻，这机器不再只服务一个用户。它要同时给整个网络的用户提供打印服务。这些用户也不再老老实实地站在机器前面，而是坐在网络的另一端，隔着老远，向这台机器发布打印命令，指望它能按要求完成任务。等这些用户回过神，想起去取打印的文件时才会发现，大半的内容都被一页纸卡住出不来了。

在这台打印机之前，斯托曼也遇到过卡纸问题，他也是实验室里第一个提出解决方案的人。几年前，实验室还用着一台旧打印机，也有类似的问题。这台打印机的控制程序，运行在实验室里的一台PDP-11计算机上。那会儿，斯托曼修改了这个控制程序，解决了这个问题。当然，他没法直接修理打印机来解决卡纸的问题。不过他能修改控制程序，让它定期检查打印机是否工作正常，再把检查结果传给实验室的核心计算机——一台PDP-10。生怕哪个粗心用户忘了去查看打印机，斯托曼还让控制程序在卡纸的时候，向所有等待打印任务的用户发送一条提醒消息。消息简短明确：“打印机被卡住了，请去维修。”收到这消息的人都是等着要用打印机的，所以问题就迎“人”而解。

斯托曼这解决方案虽然治标不治本，但也算讨巧。它没解决打印机机械部件的问题，却提出了一个次优方案：完善人机交互，及早报告问题。多亏了斯托曼加的几行代码，人工智能实验室的员工，不用再跑来跑去地查看打印机状态了。这样，每周起码节省了10～15分钟时间。用编程的术语讲，斯托曼的方案提高了网络的整体智能。

“你要是收到这条消息，你可就坐不住了。你多半等不及别人去解决卡纸问题，”斯托曼回忆着其中的逻辑，“你得亲力亲为，跑到打印机跟前。一两分钟之后，要是问题还没解决，就会聚来两三个人。这其中，总会有个人知道怎么修理。”

类似的巧法子是人工智能实验室的一大特色。尤其在其中的资深程序员之间，屡见不鲜。实际上，那些顶尖程序员不屑于用“程序员”这词。他们更喜欢用圈子里的行话，自称“黑客”。这词儿涵盖了不少内容：从抖机灵、甩包袱，到改进现有软件，优化计算机系统。而更深之处，则蕴含着旧时美国移民的智慧。对于黑客来说，有这样一条铁律：从头开发一个软件只是小儿科；改进一个程序才显真本事\[1]。

这条铁律，恰恰影响着施乐这样的公司，让它们乐意把自己的产品，以及配套的软件捐赠到黑客聚集的地方。要是这些黑客们改进了其中的软件，这些公司就可以把这些修改拿过来，化为己用，投入市场。用商业术语讲，这叫优势社会资产。公司花小钱，就能有个附属研发部门。

凭着这份礼尚往来的精神，斯托曼在这台新打印机面前并不慌张。他只要找个法子，把以前那套修改方案拿过来，修理修理这机器，或者用圈子里的话说，“黑”它一下，就万事大吉了。可是，他刚找了找这台施乐激光打印机的软件，就碰了一鼻子灰。这打印机根本不提供软件，至少没提供任何给人读的程序代码。要知道，那个时代，大多数公司都会发布软件的源代码（一系列可供人阅读的文本文件，用于详细定义程序的行为）。可当下，施乐公司提供的程序，却只有编译好的可执行文件。程序员倒是可以打开这些文件，可打开之后看见的，全是0和1。除非他们有闲功夫，乐意去翻译这些二进制信息，否则这些东西看起来只是一堆胡言乱语。

尽管斯托曼可谓是精通计算机，但还是没那份闲心和时间去解释这些二进制文件。不过作为一名黑客，他总是有法子。他知道，黑客这个圈子里，分享信息是至关重要的。过不了多久，就会有个黑客，从大学实验室或者哪个公司的机房里，拿出这激光打印机控制软件的源代码，分享给圈子里的同胞。

经历了几次卡纸事件之后，斯托曼还耐着性子安慰自己。不管怎么说，当初也遇到过类似情况的。几年前，实验室需要一个网络程序，让那台PDP-11和PDP-10之间协调工作。实验室里这群黑客自然能胜任这项任务。不过，作为一名哈佛毕业的校友，斯托曼记起了当初在哈佛计算机系，有个黑客也写过类似的程序。就运行在哈佛的一台PDP-10上。那台PDP-10，和当下人工智能实验室这台一样，只是运行了不同的操作系统。哈佛的机房里有规定，要求所有安装在PDP-10上的程序，都必须发布源代码。

作为校友，斯托曼还可以进哈佛的机房。他就大模大样地走进去，复制出源代码，带回了麻省理工的人工智能实验室。紧接着，他改写了程序，让它能在人工实验室的机器上运行。不费吹灰之力，人工智能实验室的软件设施又进步了一截。斯托曼甚至还在哈佛的软件基础上，增加了点新功能。“后来这个程序我们用了好几年。”斯托曼回忆道。

对于20世纪70年代的程序员来说，把软件复制来复制去，就好比从邻居家借碗酱油那样稀松平常。所不同的是，你从邻居那拿了多少酱油，邻居就少了多少。而从别人那里复制一个程序出来，并不影响别人继续使用那个程序。要说有影响，也是正面的。因为斯托曼对这程序还加了些功能，别的黑客可以自由地复制斯托曼改进的程序。这也算礼尚往来了。在哈佛那边，后来确实有个从Bolt,Beranek & Newman这家公司来的程序员，复制走了斯托曼的程序。之后还又加了点功能，斯托曼则又把改进后的程序复制了回来，用回到人工智能实验室里。

“开发一个程序就好比开发一座城市，”斯托曼回忆着人工智能实验室的软件设施，“有些部分会被换掉，有些得重建翻修。新的东西会逐步加进来。可如果你仔细看某个部分，也许会感慨这块从风格看应该是20世纪60年代早期的；之后的部分估计是70年代中期完成的。”

圈子里的这种氛围简单朴实，它让知识逐渐积累。这种积累为以后的发明和创造提供了稳固的基石。人工智能实验室以及世界各地的黑客们，都得益于这个氛围。比如在美国的西海岸，一群加州大学伯克利分校的计算机科学家们和AT & T的工程师合作，遵循着如此积累知识的理念，创造了一整套操作系统。他们把这操作系统叫作UNIX。UNIX这个名字来源于另一个操作系统的名字——Multics，一个早期的学术研究项目。倘若是当初的程序员，只要愿意支付成本价和运输费，就可以买到一份UNIX系统的副本。整套系统会被复制到一个全新的磁带上，完整地寄到购买者手里，谁都能买，童叟无欺。参与到这个文化小圈子的程序员，不一定都把自己称为黑客。不过，绝大多数人都有着斯托曼那般的情结：要是一个程序或者一个补丁可以解决自己的问题，没准也能帮到别人。独乐乐不如众乐乐，何不分享给大家，起码也算积德行善了。

一开始，施乐公司不分享源代码的行为倒也没惹到谁。斯托曼在找源代码的过程中，甚至都没想过去联系施乐公司：“人家都送咱打印机了，何必还非得兴师动众地管他们要代码呢？”

可是眼巴巴地等着源代码，如今还没找到，倒是让斯托曼起了疑心，勾起了他几年前一段不快的回忆。当初，一位在卡耐基梅隆大学的计算机博士，名叫布莱恩・瑞德（Brian Reid）。他开发了一个很不错的文本排版软件，名叫Scribe。这软件可以让用户通过网络传递文档并且还支持自定义的字体，这在当时可是首例。之后这种功能的普及则带来了HTML——如今WWW网络上的通用语言。1979年，布莱恩决定把Scribe出售给一家在匹兹堡的公司，名叫Unilogic。他当时刚好博士毕业，正打算把开发Scribe的任务转手给别人，免得它流落到公有领域里。为了让这份订单更吸引人，布莱恩在Scribe中动了点小手脚：他在里面放了个“定时炸弹”，让用户有90天的免费试用期。90天一过，如果用户不交费，则不能再使用这个软件。

对于布莱恩来说，这个买卖是个双赢策略。一方面，正如布莱恩所期望的那样，Scribe的代码的确没有流落到公有领域；另一方面，Unilogic也有了一个向用户收费的途径。可这对斯托曼来说，这份交易完全是背叛了程序员的良心。布莱恩非但没遵循分享再传播的精神，而且竟然还助纣为虐，帮助公司去强制限制用户自由。

一周过去了，依然没有施乐激光打印机源代码的一丁点消息。斯托曼觉得这好像又是一笔索财要钱的勾当。不过还没等他给这事定性，好消息就来了：一个在卡耐基梅隆大学，计算机系的教授刚刚从施乐公司离开。这位教授还在激光打印机部分工作，而且从收到的八卦消息看，他在卡耐基梅隆大学还在继续激光打印机方面的研究。

于是，斯托曼这才抛开之前的胡思乱想，打算下次去卡耐基梅隆大学的时候，去会见这位教授。

也没多久，他就得到了一次访问卡耐基梅隆大学的机会。和斯托曼所在的麻省理工学院一样，它们那里也有一个人工智能实验室。这才几个月不到，斯托曼就因为工作原因需要去卡耐基梅隆大学出差访问。访问中，他在计算机系请人帮忙找到了那位曾在施乐公司领导激光打印机项目的教授。他正好就在办公室。

工程师之间的讨论总是开门见山的。几句简单寒暄过后，斯托曼就直入主题，说明自己是为了激光打印机的控制程序代码而来，以便可以修改后用到麻省理工学院的PDP-11计算机上。可令斯托曼吃惊的是，这位教授竟然拒绝了他的要求。

“他跟我说他答应了公司不能泄露代码。”斯托曼说。

记忆总是这么有趣。二十年过去了，斯托曼关于这段经历的回忆大部分都是空白的。他都不记得当初为了什么事去的卡耐基梅隆大学，连具体哪年去的都给忘了。他也不记得那位教授是谁。根据Scribe的作者瑞德的回忆，惹到斯托曼的那位很可能是罗伯特・斯布鲁（Robert Sproull）。他曾是施乐公司PARC研究所的研究员，如今在Sun研究所任部门主管。20世纪70年代，斯布鲁在施乐公司PARC研究所负责激光打印机程序的主要开发。他在80年代拿到了卡耐基梅隆大学的教职，并在那里继续他的激光打印机相关的工作。

“斯托曼想要的代码包含的可都是前沿技术，那可是斯布鲁去卡耐基梅隆之前，花了几年的时间研发的成果，”瑞德回忆道，“我想斯托曼拜访斯布鲁那会，他刚刚到卡耐基梅隆大学还不到一个月。”

可是，直接给斯布鲁发邮件，询问当初的事情，他却不记得这事了：“实在是无可奉告。”斯布鲁在邮件中写道：“我确实不记得有这么一件事。”

当事双方谁也不记得事情的细节，甚至都无法确定是否真的发生过。至于斯托曼说的，斯布鲁硬生生地拒绝了他的这件事，也就无从考证了。在之后的各种演讲中，斯托曼一再提及这件事。强调斯布鲁由于签署了保密协议，从而不能泄露源代码。如今在各个IT公司，签署保密协议已经非常普遍。不过在当时，为软件代码签署保密协议还算先例。这也间接地反映出施乐公司对激光打印机项目的重视程度。“施乐公司打算把激光打印机做成商业产品”，瑞德说，“他们除非疯了，才会把代码泄露出去。”

但在斯托曼看来，这种保密协议完全是另外一回事。那时大家都把软件认为是一种共有的资源，卡耐基梅隆大学一些研究员的做法，就意味着否定这个公理。这对斯托曼来说，就好比是一个农夫眼看着用来灌溉庄稼的河流干枯了，循着河道往上巡查，竟然看到一道大坝从天而降，拦住河水。大坝上赫然印着几个大字：施乐公司。

施乐公司用各种花言巧语，把一位程序员同胞带入了这片新天地，与世隔绝。不过一开始，斯托曼也没把重点集中在施乐公司那边，而是怪罪到了个人性格上。作为一个标准技术宅男，斯托曼和人沟通起来难免有点障碍。他这次亲自跑去拜访一位程序员同行，已经是一种充满诚意的行为了。而到头来却被当头一棒。让他实在觉得对方有点鲁莽。“我当时非常生气，都不知道怎么表达。我二话没说，扭头就走了，”斯托曼说，“没准我还使劲摔了门，谁知道呢。我能记得的，就是当时想赶快离开。”

二十多年过去了，斯托曼当初的怨气还在。他甚至把这个事件描述为人生转折点。然而，那之后几个月中，在人工智能实验室以及斯托曼身上发生的各种事，却比这次打印机事件还令人难以接受。斯托曼，本是一名孤独的黑客，本能地对绝对权威存有戒心。在经历了这一系列事件后，他变成了一位斗士，把传统的自由、平等、博爱的精神引入软件开发领域。而这次的打印机事件，在其一生的无数事件中则最值得一书。

“它让我思考了一些脑海中由来已久的问题，”斯托曼说，“我以前有过一些初步的想法，认为软件本该共享。可当时还不知道怎么表述。那时的想法还没有清晰到可以用简单几句话给别人介绍。”

尽管之前也有过类似的不快经历，可这次的打印机事件彻底让斯托曼意识到，这一系列的事件，正悄悄地侵蚀自己所珍视的文化——那个神圣不可侵犯的小圈子。作为一名世界顶级研究机构的顶级程序员，斯托曼之前一直都无视那些程序员同行所作的各种妥协让步，因为他们还不至于影响到斯托曼的工作。而如今施乐激光打印机的到来，让斯托曼开始注意到其他计算机用户一直忍受的程序和机器。这些程序很少能影响到人工智能实验室，斯托曼和实验室的成员之前一直都可以自由地重写软件，添加功能。直到有一天，人工智能实验室把一台计算机的操作系统从不相容分时系统（Incompatible Time Sharing Operating System）换成了商业的TOPS 20系统，这些就再也不能做了。

如今，这台激光打印机已经强势入驻到人工智能实验室了，而外面的世界也悄悄发生了变化。除了偶尔卡纸以外，打印机工作还算正常。可是按照个人喜好修改软件则不可能了。从软件业的角度看，这台打印机的出现是个信号，预示着软件是公司的重要财产。谁也不会再想发布软件源代码，因为这可能会给潜在竞争对手机会，让他们可以轻松山寨自己的产品。而在斯托曼看来，这台打印机简直就是个卧底。十来年的尝试，私有软件总算在人工智能实验室中站得一角。私有软件，也就是如今所说的专有软件，这次被打扮成礼物，潜入得悄无声息。

施乐公司后来还发出邀请，让一些程序员再使用它们的礼品。斯托曼说，要是再早几年，他没准也无法拒绝这种免费午餐。是那次打印机事件，让斯托曼建立起了道德防线。它不仅给了斯托曼足够的怒火去对以后的各种礼品心存戒备，更让斯托曼开始思考一个让他自己也坐立不安的问题：要是以后哪个黑客同行进到自己的办公室，向他索要代码，他究竟会不会拒绝复制代码呢？

“这是我第一次碰上这种保密协议，它很快让我明白，保密协议面前，总会有无辜的受害者”，斯托曼坚定地说，“在打印机事件中，我和整个人工智能实验室扮演了受害者的角色。”

斯托曼带着这种态度，经历了动荡的20世纪80年代。在这期间，麻省理工学院的同事们纷纷离开实验室，走进公司，签署了保密协议。大多数保密协议都有解密时间，而这则成了很多黑客们的借口。他们会辩解说：软件迟早会成为公共资源。而保证软件在早期的开发阶段不被泄露，则可以保证让各位黑客朋友们可以进入顶尖项目中工作。这些借口，在斯托曼看来，则是迈向深渊的第一步。

“要是谁跟我建议，让我以这种方式背叛我的同事，我就会回忆起在打印机事件中，我和我的同事被别人背叛的感觉，那份怒火终生难忘”，斯托曼说，“我会回敬给分发专有软件的人，并告诉他‘谢谢你的软件，非常棒！可是我不能接受你的那些保密协议，很遗憾，我不会用它。’”

斯托曼很快就会明白，要拒绝这些要求和邀请，不仅需要一些个人牺牲，更会被其他一些黑客们疏远。这些黑客虽然也对各种保密协议嗤之以鼻，但会更圆滑地对它加以评判。正因为如此，斯托曼被誉为“最后的黑客”。这使他与专有软件市场渐行渐远。拒绝提供源代码，在斯托曼看来，不仅违背了第二次世界大战以来深植入软件开发中的科学精神，更违背了“己所不欲，勿施于人”的道德准则。

打印机事件的重要意义恰在于此。正如斯托曼所言，倘若没有这次的事件，他的人生也许就会落入平常，纠结着，一边开发专有软件，一边痛苦地编写没人会看到的代码。当然也不会有着如今清晰的思路，更不会去解决别人从未想过的各种问题。最重要的，他心中也不会再有那份不平，推动着他去追求他的政治理想和道德信仰。

“从那日起，我决定绝不参与其中”谈起软件保密协议和类似的事情，斯托曼如是说，在他看来，这是一场以个人自由换取便利的交易，“我决定绝不让第二个人为此成为像我一样的受害者。”

注　释

\[1].要深入了解“黑客”这个词，参阅附录B。
