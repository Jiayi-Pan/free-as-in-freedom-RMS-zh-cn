# 第8章 ST.IGNUCIUS

茂宜高性能计算中心（Maui High Performance Computing Center）坐落在夏威夷群岛中的茂宜岛上。这是一座单层建筑，建在满是红色火山灰的山岗上，俯瞰茂宜岛的商业中心纪平镇。这个计算中心身在夏威夷，坐拥迷人的山景海风，更有身价千万的房产。这地方好像和高新技术沾不上一点边。它跟麻省理工学院技术广场的见楞见角、死气沉沉的气氛完全不同。哪怕跟阿尔贡国家实验室，洛斯阿拉莫斯或者新墨西哥的那些实验室比，茂宜高性能计算中心依旧显得特别。总会难免让人觉得，茂宜计算中心的科学家们每天可能并不怎么关心自己的研究课题，没准他们天天都会把时间花在晒太阳、吹海风上。

不过，这个第一感觉可不怎么准确。确实，茂宜计算中心的研究人员的确占尽了地利，也自然会借此休养。不过，他们对待工作还是非常认真的。Top500.org是一个记录全世界超级计算机排名的网站。根据这个网站的资料，茂宜高性能计算中心的IBM SP Power3超级计算机可以每秒完成八千三百七十亿次浮点运算，世界排名前25。这台超级计算机归夏威夷大学和美国空军共同拥有和维护。它主要负责完成军队补给调度计算和高温物理研究。

简而言之，茂宜计算中心是个非常独特的地方。这地方既有学术研究的文化氛围，又融入了夏威夷上那份慵懒宜人的情调。二者一阴一阳，相得益彰。2000年，他们在自己的官方网站放上了这样一条标语：在天堂之上计算。

这样一个地方，一般你是见不到理查德・斯托曼身影的。他这次来到这里，站在一位员工办公室的窗口，盯着外面如画的风景，口中却蹦出了一句简单的批评：“阳光太强。”自然，他从计算机界的圣地麻省理工学院来到这里，是有话要讲的。哪怕再强的阳光，暴晒着这位黑客的苍白的皮肤，他也在所不辞。

我赶到现场的时候，会议室里早已人满为患，大家都在等待着斯托曼的演讲。听众中，男女比例倒是比纽约那次的演讲平衡些，不过也没平衡到哪儿去：大约85%是男性，15%的女性。有一半的听众，都身穿土黄色的裤子，配上印着商标的高尔夫衬衫。另外一半，则显得更加融入了当地的风俗。身穿宽大的大花T恤，皮肤则已被晒成了褐色。这打扮在夏威夷可是正常装束。唯一能显示他们技术本色的东西，也就只剩下了些小玩意儿了：诺基亚手机，掌上电脑，还有索尼VAIO笔记本。

斯托曼身穿纯蓝色T恤，棕色涤纶休闲裤，白色袜子。不用说，这身行头在当下确实太显眼了。房间中淡淡的花香，倒是让人没太注意斯托曼缺少阳光滋润的皮肤。不过，他的一头长发和络腮胡须却依旧能引人注目。外人一看，就知道他不是本地人。他就差在脑门上贴个标签，写着：美国本土人士。演讲开始前，斯托曼自己在会议室前面闲逛。旁边几个人鼓捣着录像录音器材。这些人都身穿“茂宜FreeBSD用户组”（Maui FreeBSD User Group，MFUG）的T恤。所谓FreeBSD，是一款从伯克利软件发行版的UNIX系统分支而来的操作系统。而伯克利版UNIX则是20世纪70年代由加州大学伯克利分校开发的一个UNIX分支。说起来，FreeBSD倒还是GNU/Linux的一个竞争对手。在黑客的世界里，斯托曼的演讲总会被记录拍摄下来，留作档案。作为当地的著名自由软件组织，茂宜FreeBSD用户组可不能让同行失望。他们也要录音和录像，让远在德国汉堡、印度孟买、俄罗斯新西伯利亚等世界各地的黑客们都能听到RMS的箴言。

斯托曼的这些演讲记录，就像感恩而死乐队（Grateful Dead）的现场演出一样，都是被追捧者现场录下、私下传递的。把斯托曼和感恩而死乐队做类比，可是有说头的。每当斯托曼描述自由软件的商业盈利模式的时候，他都会提起感恩而死乐队。这个乐队当年允许粉丝们在现场录音和录像，这就令它不仅是一个简单的摇滚乐队。它俨然成了感恩而死音乐部落的中心。逐渐地，这个部落越来越大，令感恩而死乐队拒绝了各种唱片公司的合约，完全靠巡回演出，就可以撑起整个乐队的开支。在1994年，这支乐队的最后一次演出仅门票收入就高达五千两百万美元\[1]。

当然，还没有哪个软件公司的成就可以媲美感恩而死乐队。不过，自由软件社区的这个部落越来越大，20世纪在90年代后期，大家也逐渐开始认为分享发布软件的源代码没准是个好事。各大公司纷纷出马，企图建立起各自的忠实粉丝群。这其中就包括IBM、Sun、惠普等。它们也许并没有打心眼里接受自由软件的看法，但他们的行为却是在响应斯托曼的号召。ZDNet的软件专栏作家埃文・列伊博维奇（Evan Leibovitch）把GPL（GNU通用公共许可证，斯托曼创立的一种自由软件许可证，用于规定软件作者授予软件用户的各种权利）描述为信息时代的大宪章。他认为，人们对于GNU的拥护持续高涨，并非单纯地跟风。他曾写道：“这个趋势让用户可以重新掌控自己的命运。就好像当年《大宪章》给了英国人民权利。GPL让消费者作为计算机软件用户有了自己的权利和自由\[2]。”

自由软件社区的这种部落文化也解释了为什么今天这四十来位古怪的程序员们，可以暂时不管各自的工作，也不去上网冲浪，而宁愿能挤在这个会议室里听斯托曼的讲座。

和那次在纽约的讲座不一样，这次没有人为他做开场白，斯托曼自己也没做自我介绍。FreeBSD用户组的人把设备一架好，斯托曼就自己踏上前来，开始演讲，声音一下盖过了台下的私语。

“一个社会该给软件的使用设立何种规则？每当想到这个问题，大多数人总是站在软件公司的立场思考。他们的想法往往像是在自我圆场，”斯托曼开门见山，“他们想：我们如何设立规则，才能让大家多给我们钱呢？我很幸运，在20世纪70年代曾加入了一个大家庭，在那里大家都会互相分享软件。正因为如此，我总会从另外一个角度去思考这个问题：我们应该如何设立规则，才能帮助我们构建一个更好的社会，一个可以让每个人都受益的社会？也正因为如此，我得到了完全不一样的答案。”

斯托曼又一次提起了施乐打印机事件，形式和以前很像，同样是讲到最后，手指指向听众，口中说着：“也许就会背叛你！”之后，他又花了一两分钟，来解释GNU/Linux的名字问题。

“有些人会和我说，‘你为什么要花这么多精力去在乎人们叫它什么？为什么非要在乎这种名利上的事？如今任务已经做完了，你何必非要在乎人们有没有注意到GNU呢？’这个……如果这话描述的是事实，那我确实同意这话的观点。可现实是：我们的任务并没有完成。我们的任务不是要创造一套操作系统；我们的任务是要给计算机用户自由。要完成这个任务，我们必须要尽一切努力，让用户可以自由地使用计算机和软件\[3]。”

斯托曼最后说：“我们要走的路还很长。”

对于一些听众来说，斯托曼的这些话是老生常谈了。对于其他人来说，这些话则有点令人不可思议了。旁边那个身穿高尔夫T恤的听众已经开始打盹了，斯托曼停下来，让旁边的人把这位叫醒。

“曾经有个人，说我的声音特别像安慰剂，他问我是不是做过催眠师之类的工作，”斯托曼说着，下面一阵笑声。在笑声中他接着说，“我想这意味着我可以帮你们快速进入梦乡。可能你们之中有些人正想要这样。我觉得我确实也不该打搅你们，你要是真想睡觉，尽管睡吧。”

演讲最后，斯托曼简要地探讨了软件专利的问题。这个问题逐渐在软件业和自由软件社区中受到关注。专利的概念和想法本是为现实的物理世界准备。可是，如果把它用在信息世界中，就越来越显得古怪了。软件版权和软件专利这两个概念看似差不多，实则差距甚远。创作者可以借助版权禁止他人复制自己的代码，但却无法阻止别人利用不同的代码实现相似的功能或软件。换言之，一个开发者可以从头克隆一个现有软件的所有功能。只要他不去复制别人的源代码，就不会触犯版权法。这种克隆想法或功能的行为非常普遍。

可软件专利就不同了。按照美国专利局的说法，个人或公司的算法方面有创新想法，就可以提交专利申请，由公众来审核。理论上讲，专利拥有者需要将自己的发明公诸于众，而作为交换，专利拥有者获得法律保护，可以在二十年内禁止他人实现这个想法，计时从专利提交起开始。当年专利法设立的初衷是为了避免优秀的想法被当作商业机密封锁在公司内部，不被大众所用。但是实际上，到了软件领域，这个事情就变了样。软件专利的创新想法并不能让公众受益。因为大多数软件专利中提到想法往往是不言自明的。而专利法和版权法不同，它禁止任何人实现专利上描述的想法，哪怕开发者是独立开发的。

在软件世界里，二十年的时间可能覆盖了一个市场的整个生命周期。这样，专利就成了一种策略。当年，微软和苹果这些大公司为版权打得不可开交。而如今那些互联网企业，则使用专利来为自己开路，赶走竞争对手和新人。这里有个著名的案例：2000年，亚马逊购物曾试图为它的“一键购买”功能注册专利。简单地说，这个功能就是允许用户事先存储好个人信息——比如信用卡信息、收件人地址等——然后在购买商品的时候，只需要按一个按钮，就可以下单，不必再跳转到其他页面填写地址、付款等信息。对于大多数公司来说，软件专利更像是一种防卫措施。几个公司可能会合作共有一系列专利，用来阻止另外一个联盟的专利。尽管如此，还是有不少领域被软件专利占满，阻碍了各种可能的竞争对手，如图像处理领域、加密领域等。

对于斯托曼来说，软件专利更督促着黑客要时刻警觉，而且还平添了几分戏剧色彩。也恰恰是软件专利，让自由软件一直强调的政治策略再次得以重申。即，用户的自由比其他东西更重要。斯托曼说，软件专利所可能造成市场的垄断，高性能、低价格等特性的确是GNU/Linux、FreeBSD等这些自由软件的优势。但是除了性能、价格这些东西以外，还有更重大的问题，那就是用户和开发者的自由。

斯托曼说：“不是因为我们技不如人，而是因为软件专利禁止我们实现很多想法，不让我们把去创造优秀的软件。遇到这个问题用户会作何感想？这要看这个用户是被哪种观念吸引进自由软件圈子里来了。一种是‘开源软件’的观念，它把软件用户的自由看作是一种工具，赋予用户这些自由，可以让软件更加强大，功能更加完善。如果用户是被‘开源’的理念打动而使用自由/开源软件的，那么当他发现某些自由软件由于专利原因，无法实现某种功能的时候，他可能会说：‘当初你们承诺软件会很强大很完善，可如今你们却没能实现这些功能，你们欺骗了我！’与‘开源’的理念不同，‘自由软件’强调软件用户的自由本身的重要性，它是我们的目的，而不是一种手段。当用户了解到‘自由软件’的观点时，面对同样情况，他可能会说：‘那些软件专利怎么能如此禁止人们实现这些功能？它们怎么能这样剥夺我们的自由？’倘若用户都能如后者一般，那么面对如今和未来的大量软件专利，我们才可能生存下去。”

斯托曼的这番评论确实有些拗口。其实，大多数开源软件的支持者其实也一样反对软件专利。但关于开源软件和自由软件的区别，斯托曼的描述却也不错：开源软件的观念更偏向于实用主义；而自由软件的观念则更强调用户自由。开源的支持者不怎么喜欢强调软件用户的自由，他们更愿意强调黑客开发的工程模型。强调同行互相审校的重要性。他们认为，GNU/Linux或FreeBSD的开发模式可以创造出更好、更强大、更值得信赖的软件。

但是，“开源”一词也并非意味着没有任何政治诉求。对于开源支持者来说，开源有着两重含义。第一，它避免了在英文中使用Free一词。自由软件的英文是Free Software，因为Free在英文中既有自由的意思，也有免费的意项，所以难免会产生歧义。很多商业公司会觉得自由软件等于免费软件。使用“开源”一词的动机之一，就是希望消除这种歧义。第二，它让商业公司可以从技术角度去审视自由软件，而不必在道义上过多解读。埃里克・雷蒙德（Eric Raymond）是开放源代码促进会（Open Source Initiative，OSI）的联合创始人之一，也是支持使用“开源”一词的著名黑客。他曾在1999年发表了一篇文章，用以表明他对遵循斯托曼的政治路线的失望。文章标题是《少说话，秀代码》（Shut Up and Show Them the Code）：

RMS（即，理查德・M・斯托曼的缩写）的用词对于我们这样的人来说很有吸引力。我们黑客都是思考者，都是理想主义者。我们都时刻准备着响应支持“自由”、“原则”和“权利”的号召。哪怕我们有时候会与斯托曼的一些意见不同，但我们依旧希望他的做法能有效。我们觉得他的言辞应该有效。可是，我们看到世界上另外95%的人和我们不一样，斯托曼的言论对他们无效。面对这些，我们开始迷惑，甚至怀疑\[4]。

雷蒙德写道：那另外95%的人中，包括很多公司经理、投资人，以及普通的计算机用户，他们不是黑客，他们会倾向于跟从专有商业软件的大市场。雷蒙德认为，如果不能赢得这些人的支持，黑客们将只能游离于主流之外，去追随自己的理想。

RMS向我们谈论起“计算机用户权利”的时候，他向我们发出了一份吸引人却危险的邀请函，引导着我们重犯旧错。我们应该拒绝它——不是因为它的原则是错的，而是因为那样的词汇用在软件上，只能说服我们自己，而不能说服别人。事实是，它把大多数圈外人都拒之千里\[5]。

看着斯托曼阐述自己的政治诉求，并不会让人迷惑或厌恶。他衣着朴素，说起话来有理有据，逻辑清晰。听众中一位提问：如果完全避免使用专有软件，可能无法用到最新的技术，该怎么办？斯托曼引述自己的信念，回答了这个问题：“我觉得自由本身比任何新近技术都重要。如果面前有一个先进的专有软件和一个技术落后的自由软件，那么我宁愿选择后者。因为无论如何，我都不会靠出卖自由，而换取更新的技术。我的原则是，如果我不能和你分享这个软件，我就不会使用它。”

斯托曼的这个回答，倒是更让我觉得他有点宗教人士的感觉。就好像是犹太人只吃洁食的行为，摩门教徒不喝酒。斯托曼仅仅使用自由软件，拒绝任何专有软件。他把这描述为个人信仰，并且希望把这份信仰与大家一同分享。但他不会强迫别人认同自己。大多数听众，在听过斯托曼的演讲之后，都会明白斯托曼所说的正确的软件之路。

演讲最后，像个总结一样，斯托曼开始了一个不太寻常的仪式。他从一个百货商店的塑料购物袋里掏出了一条黑色长袍。他把长袍打开，套在了身上。接着，又从袋子里拿出来了一个圆形的老式计算机硬盘碟片，把它戴在头上。这碟片一戴上，就像极了基督教圣徒头顶的光环。看到这身扮相，人群中传来了一阵笑声。

“我是圣・IGNUcius\[6]，来自Emacs教堂。”斯托曼举起右手，好似在为众人祈福：“我保佑你的计算机，孩子们。”



![图三 斯托曼打扮成圣・IGNUcius。照片由Wouter van Oortmerssen拍摄](.gitbook/assets/image.png)

大家的笑声在几秒内变成了一阵掌声。大家在鼓掌的时候，斯托曼头上的那个硬盘碟片反射来一道强光，一下看起来，好像斯托曼头上真的顶了个光环。他眨了眨眼睛，又让我觉得他好似宗教领袖。

斯托曼接着解释道：“Emacs最开始是一个编辑器，之后，很多人把它当作一种生活方式，还有一部分人把它作为一种信仰。我们把他们称作Emacs信徒。”

很多人以为斯托曼对于自由软件一直都是不苟言笑，好像一个禁欲主义者一样。眼下这个玩笑倒是很好地否认了这种认识。在黑袍和光环之下，斯托曼好似在说：“你们尽情笑吧，我知道我这样很搞怪。”

之后，我和斯托曼聊起圣・IGNUcius这个舞台形象，他说他最早是在1996年开始在演讲中有这么个安排的。那会他早就开发了Emacs编辑器，那时也还没有“开源”这个词。斯托曼说，他当时希望能有个方式，能够“自娱自乐”一下；同时，也能告诉听众，斯托曼虽然固执，但还不至于疯狂到不苟言笑。不过这之后，一些人借着这个舞台形象，把斯托曼形容为一个软件界的空想家。埃里克・雷蒙德就在1999年的一次与Linux.com的采访中，说道：

“我说过，RMS很会算计。我并不是说他不诚实，也不是说他虚情假意。我的意思是，他和很多布道者一样，非常有舞台感。有时候，他的这种行为是有意识的——你看过他扮成圣・IGNUcius的样子吗？他身穿黑袍，把一个碟片放在头顶。还有很多时候，那是无意识的行为。他很会掌握分寸，既能让你想去反驳，又不至于把人们吓跑\[7]。”

斯托曼显然不同意埃里克・雷蒙德的说法。他说：“这不过是我自娱自乐罢了。谁要是从中还看到了别的东西，那只能说他们想多了。那都是他们脑子里的想法，不是我的。”

斯托曼也承认，他的这个表演有做作的成分。“就是开个玩笑。我很享受被万众瞩目的感觉。”他如是辩解。为了让自己的演讲技能可以更加娴熟，他甚至还加入过Toastermasters。这个社团旨在帮助人们提高演讲技能。斯托曼也曾向别人建议过Toastermasters。他加入了这个社团，逐渐掌握了一些舞台技巧。在这次茂宜高性能计算中心的演讲之后几天，我和斯托曼聊天的时候，问起他是否有种所谓的“格鲁桥・马克思情结”——就是像著名喜剧演员格鲁桥・马克思（Groucho Marx）所说的那样，拒绝加入任何希望收留他的俱乐部。斯托曼立即回复道：“不，但是我在很多方面都很敬仰格鲁桥・马克思，我说过的很多话都曾受到过他的启发。不过，我也受到过汉普・马克思（Harpo Marx）的启发。”

斯托曼一直以来对俏皮话、双关语的喜爱，恐怕的确是受了格鲁桥・马克思的影响。不过话说回来，双关语和文字游戏也从来都是黑客们的最爱。要说斯托曼真是有哪点会像格鲁桥，恐怕是他开玩笑之后，那副依旧淡定的表情。他的那些玩笑总是在不经意之间蹦出来，他自己则一脸严肃，眉毛都不抬。在你笑过之后，甚至反而会觉得斯托曼正在内心中笑话你。

不过你别担心，斯托曼可没笑话你。看到他在茂宜高性能计算中心演讲时候的圣・IGNUcius的扮相，你的顾虑就打消了。他这表演虽然不比单口相声，但斯托曼总还是有能耐把一屋子的工程师聚在一起。“Emacs教会之中，不必戒色禁欲。但也需你心存底线，道清德厚，有所顾忌。”斯托曼继续对听众说道：“你要在自己的电脑之上，趋邪扶正。专有软件，卸载删除。辟得净土，以敬用户。系统上下，软件自由。茫茫众生，守此信条，即入本会，得道称圣。对了，到时候你没准也能拿到这样一个光环。”

圣・IGNUcius的演出以一个圈内冷笑话做结尾。在大多数UNIX或者类UNIX系统上，和Emacs齐名的另外一款编辑器名为vi。vi编辑器最早是由比尔・乔伊开发。他当年是加州大学伯克利分校的学生，如今是Sun微系统公司的首席科学家。斯托曼在摘掉自己头顶的“光环”之前，给vi这个竞争对手开了个小玩笑。“人们会问，在Emacs教会中使用vi是否算作原罪。倘若使用的是自由版的vi，那不能称之为罪。可以算是自罚赎罪。那么，Happy Hacking!”

一个简短的提问环节过后，听众们围在斯托曼周围，有些人向他索要签名。斯托曼拿着一位女士打印出来的GNU通用许可证，说：“我可以答应你在上面签名，不过你要答应我，在指代那整个操作系统的时候，使用GNU/Linux这个词。并且要告诉你的朋友也这么做。”

他的这个举动倒是证实了我的想法。和演员、政客不同，斯托曼的行为会始终如一，不会切换到“台下模式”。在圣・IGNUcius这个角色中看到的那份理想主义，会一直体现在斯托曼的每个言行之上。在演讲之后的晚餐上，一位程序员向斯托曼提起了自己参与“开源”软件的经历，斯托曼还没顾得上咽下嘴里的食物，说道：“你是说自由软件吧。用自由软件这个词恐怕更恰当。”

在演讲结束后的提问环节，斯托曼承认自己很多时候有些咬文嚼字。“很多人会劝我：‘咱们先把人邀请进我们的圈子，然后再教会他们什么是自由。’这也许是个好策略，但是我们当下的情况是，基本所有人都在邀请朋友们进到这个圈子里，可却没有几个人会告诉朋友自由是什么。”

最后的结果，用斯托曼的话说，就是好比很多第三世界国家建立的城市。人们怀揣梦想从四面八方涌入城市，希望能让自己的生活变得更加富裕，或者至少能融入到这个充满活力和开放文化的社会，但是那些真正有权有势的人则通过制定各种新的方针政策来玩弄老百姓。软件专利就是一个很好的例子。“你把百万千万的人扔到城市中，结果是在城市里建起了成千上万的城中村、贫民窟。但是没人开始着手做下一步的工作：把城中村，贫民窟里的人解救出来。如果你觉得讨论软件用户的自由是有意义的，那么请加入我们，开始做第二步工作。很多人都在做第一步，但这第二步却无人问津。”

这“第二步”工作直指自由软件运动的核心：自由软件的重点并非是装机量用户量，而是赋予用户自由。有些人希望能从内部瓦解整个专有软件工业，这实在是痴人梦话。斯托曼说：“从内部瓦解实在不现实，除非你能像当年戈尔巴乔夫那样攀到高位，否则你多半会被同化。”

又有很多人举手提问，斯托曼随机选择了一位身穿高尔夫衬衫的听众，这位听众问道：“如果没有专利，你会建议如何防止商业间谍？”

斯托曼答：“嗯……这其实是两个互不相关的问题。”

提问者补充道：“我是说，如果有人想要窃取另一个公司的软件。”

斯托曼立即反应道：“等等，你说‘窃取’？不好意思，你的这番陈述里包含太多偏见了。我只能说，我很难认同这些偏见。各个公司，它们可能会开发专有软件，或者开发任何别的东西。无论开发什么，多少都会有些商业机密，它们无论如何都会保守这些机密。这个事实恐怕很难改变。在早年间——哪怕到了20世纪80年代——绝大部分程序员都没想到过把软件去申请专利。人们会发表文章记录自己有趣的想法，如果他们不认同自由软件的理念，他们可能会在文章中甚少提及各种细节。如今，他们同样写篇文章，笼统地记录下那些想法，依然保守着各种细节。如今不同的是，他们把这文章拿去专利局，就可以申请下专利。软件专利并没能把这个事实改变多少。”

“但如果不会影响他们公开发表的文章……”另一位听众起立发言，但还没说完，就被打断了。

“但它的确影响了，”斯托曼说，“在版权局能查到的公开文章就是告诉你，从现在开始往后二十年，这个想法任何人都不能随便用。这能算是什么好处吗？还请注意，他们在文章中，会把想法描述得像天书一般难懂，而且会尽量把话说得模棱两可，这样就可以让这版权覆盖尽可能多的地方。没有几个人会从那些文章里去学习哪个版权所保护的技术。你能从那些文章中了解到的信息，只能告诉你什么技术你不能用。”

听众一时安静下来。这个演讲从下午3:15开始，现在已经将近五点。下面很多听众已经有些坐不住了。斯托曼也察觉到了听众的倦意，他目光扫视了全场，说道：“那么，今天就到这儿吧。”他又停顿了一下，等到确认没有人有问题之后，斯托曼又重复了一遍那句口头语。

“Happy Hacking。”斯托曼说。

注　释

\[1].参见《1985年～1995年北美演出收入排行榜》，http://www. dead101.com/1197.htm。

\[2].参见埃文・列伊博维奇在文章《谁会害怕大灰狼》（Who's Afraid of Big Bad Wolves），2000年12月15日，ZDNet Tech Update. http://www.zdnet.com/news/whos-afraid-of-the-big-bad-wolves/298394。

\[3].为了叙述方便，我（原作者）一直没有机会详细介绍斯托曼所说的自由软件。在GNU项目的网站上，定义了软件用户的4个基本自由：• 出于任何目的而运行软件的自由（自由度0）；• 阅读、学习并且修改软件源代码的自由（自由度1）；• 将软件对外发布的自由（自由度2）；• 将修改后的软件对外发布的自由（自由度3）。想要了解更多信息，参见GNU项目网站上的《自由软件定义》：http://www.gnu.org/philosophy/free-sw.html。

\[4].参见埃里克・雷蒙德于1999年6月28日发表在网络上的短文《少说话，秀代码》。

\[5].参见埃里克・雷蒙德于1999年6月28日发表在网络上的短文《少说话，秀代码》。

\[6].译注：圣・IGNUcius（St. IGNUcius），名字中包含了GNU三个字母。这个名字可能来自基督教圣人伊格那丢（St. Ignatius）。伊格那丢被罗马皇帝投入野兽笼中而死。斯托曼的圣・IGNUcius本身并没有任何宗教意义（斯托曼本人是无神论者），仅仅出于玩笑心理，起了这么个名字：既能在字面上和基督教圣徒有些类似，又能把GNU三个字母放进名字里。

\[7].参见1998年5月18日刊登于Linux.com的文章Guest Interview:Eric S. Raymond：http://www.linux.com/interviews/19990518/8/。
