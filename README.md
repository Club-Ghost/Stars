[index (2).html](https://github.com/user-attachments/files/28335334/index.2.html)
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>3D坦克 - 明星玩家殿堂</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Microsoft Yahei", sans-serif;
        }

        body {
            background: #080c1a;
            background-image: 
                radial-gradient(circle at 20% 10%, rgba(0, 150, 255, 0.1) 0%, transparent 40%),
                radial-gradient(circle at 80% 90%, rgba(138, 43, 226, 0.1) 0%, transparent 40%);
            min-height: 100vh;
            padding: 40px 20px;
            color: #fff;
        }

        /* 页面标题 */
        .page-title {
            text-align: center;
            margin-bottom: 50px;
        }
        .page-title h1 {
            font-size: 42px;
            letter-spacing: 6px;
            background: linear-gradient(90deg, #00d8ff, #9d00ff);
            -webkit-background-clip: text;
            color: transparent;
            text-shadow: 0 0 30px rgba(0, 200, 255, 0.5);
            margin-bottom: 12px;
        }
        .page-title p {
            color: #8ab4f8;
            font-size: 16px;
            letter-spacing: 2px;
        }

        /* 玩家容器 */
        .player-container {
            max-width: 1400px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
            gap: 30px;
        }

        /* 玩家卡片 科技风主体 */
        .player-card {
            background: rgba(15, 25, 50, 0.7);
            border: 1px solid rgba(0, 180, 255, 0.3);
            border-radius: 16px;
            padding: 28px;
            backdrop-filter: blur(8px);
            position: relative;
            overflow: hidden;
            transition: all 0.4s ease;
        }
        .player-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(0, 220, 255, 0.15), transparent);
            transition: left 0.6s ease;
        }
        .player-card:hover {
            transform: translateY(-8px);
            border-color: rgba(157, 0, 255, 0.6);
            box-shadow: 0 0 25px rgba(0, 180, 255, 0.4), 0 0 50px rgba(157, 0, 255, 0.2);
        }
        .player-card:hover::before {
            left: 100%;
        }

        /* 头部：头像+ID区域 */
        .card-head {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 20px;
        }
        .avatar-box {
            width: 88px;
            height: 88px;
            border-radius: 50%;
            border: 3px solid #00c8ff;
            box-shadow: 0 0 15px #00c8ff;
            overflow: hidden;
            flex-shrink: 0;
        }
        .avatar-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        .player-info h2 {
            font-size: 24px;
            color: #ffffff;
            margin-bottom: 6px;
        }
        .player-tag {
            display: inline-block;
            padding: 4px 12px;
            background: linear-gradient(45deg, #9d00ff, #5000ff);
            border-radius: 20px;
            font-size: 12px;
            color: #fff;
            letter-spacing: 1px;
        }

        /* 简介区域 */
        .player-desc {
            margin: 20px 0;
            padding: 16px;
            background: rgba(0, 100, 180, 0.15);
            border-left: 3px solid #00d8ff;
            border-radius: 0 8px 8px 0;
        }
        .player-desc p {
            color: #c0e8ff;
            line-height: 1.7;
            font-size: 15px;
        }

        /* 战力数据栏 */
        .player-data {
            display: flex;
            justify-content: space-between;
            padding-top: 18px;
            border-top: 1px dashed rgba(0, 180, 255, 0.3);
        }
        .data-item {
            text-align: center;
        }
        .data-item .num {
            font-size: 20px;
            color: #00f0ff;
            font-weight: bold;
        }
        .data-item .text {
            font-size: 12px;
            color: #7fa8d8;
            margin-top: 4px;
        }

        /* 底部装饰线条 */
        .line-decor {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 2px;
            background: linear-gradient(90deg, transparent, #9d00ff, transparent);
        }

        /* 适配手机 */
        @media (max-width: 768px) {
            .page-title h1 {
                font-size: 28px;
            }
            .player-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- 页面标题 -->
    <div class="page-title">
        <h1>Club 明星玩家殿堂</h1>
        <p>在逃人员· 黑榜· 完美犯罪</p>
    </div>

    <!-- 玩家列表 -->
    <div class="player-container">
        <!-- 玩家卡片 1 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55295613906_0d043c2015.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>任路嘉</h2>
                    <span class="player-tag"> 倒数|第一帅</span>
                </div>
            </div>
            <div class="player-desc">
                <p>任路嘉,化名（小帅）绰号：无.大家好，我叫任路嘉，旁人常评价我模样精神，气质洒脱，我性格直爽大方，不拘小节，很好相处，平日里热爱运动，也喜欢静下心来看看书，我待人友善，懂得尊重他人，珍惜身边的每份情谊，很荣幸认识各位，期待接下来的朝夕相伴，也希望能和大家成为要好的朋友，一起度过轻松美好的时光.</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">99999</div>
                    <div class="text">总魅力</div>
                </div>
                <div class="data-item">
                    <div class="num">99999</div>
                    <div class="text">帅气值</div>
                </div>
                <div class="data-item">
                    <div class="num">SSS+</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>

        <!-- 玩家卡片 2 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55294935041_6d64f8c4f1_b.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>张子涵</h2>
                    <span class="player-tag">黄片一哥 | 导管战神</span>
                </div>
            </div>
            <div class="player-desc">
                <p>张子涵，化名（蛋儿了）绰号：老杰了，喜欢在寂寞的时候看抖音擦边视频，并且还会进行一个视频转发，诱导别人观看擦边内容，获得情绪价值，晚上还会进行一个梦淫导致小内裤湿湿滴.</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">87210</div>
                    <div class="text">总导管</div>
                </div>
                <div class="data-item">
                    <div class="num">10520</div>
                    <div class="text">成功射出</div>
                </div>
                <div class="data-item">
                    <div class="num">S</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>

        <!-- 玩家卡片 3 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55295234318_0cf5d16910_z.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>顾雨凡</h2>
                    <span class="player-tag">美女收藏师 | 偷摸内射王</span>
                </div>
            </div>
            <div class="player-desc">
                <p>顾雨凡，化名（鹅蛋）绰号：辉宗，动漫欧美剧创始人，主打的是潜伏战术，擅长利用地形，偷偷看周围有没有可疑的人，防止小鸡暴露，进行一个导管成功.</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">92360</div>
                    <div class="text">总导管</div>
                </div>
                <div class="data-item">
                    <div class="num">11680</div>
                    <div class="text">成功射出</div>
                </div>
                <div class="data-item">
                    <div class="num">S+</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>

        <!-- 玩家卡片 4 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55295524855_3b570c6dce_z.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>顾浩噗</h2>
                    <span class="player-tag">鞋垫天花板</span>
                </div>
            </div>
            <div class="player-desc">
                <p>顾浩噗，化名（啊屁）绰号：光明，曾担任鞋垫工程师，主研究病毒性细菌鞋垫，极致输出流派，单发伤害全服顶尖，自动出现对方脚下，进行一个自动感染至死亡，堪称病毒王中王.</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">-250</div>
                    <div class="text">总战力</div>
                </div>
                <div class="data-item">
                    <div class="num">81537</div>
                    <div class="text">毒死几人</div>
                </div>
                <div class="data-item">
                    <div class="num">S</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>
        <!-- 玩家卡片 5 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55294433062_3d729b2581.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>刘笑天</h2>
                    <span class="player-tag">犟如驴 | 嘴硬大师</span>
                </div>
            </div>
            <div class="player-desc">
                <p>刘笑天，化名（犟驴）绰号：无，知名犟嘴创始人，主打口水战术喷射，擅长用嘴打遍全世界，进行左脑打右脑行为，带领战队多次使用语言攻击，犟嘴成功，圈内公认最强大嘴.</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">92360</div>
                    <div class="text">总犟嘴</div>
                </div>
                <div class="data-item">
                    <div class="num">11680</div>
                    <div class="text">胜利场次</div>
                </div>
                <div class="data-item">
                    <div class="num">S+</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>
        <!-- 玩家卡片 6 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55294433967_8fa4cb6ff1.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>杨佳旭</h2>
                    <span class="player-tag">小偷 | 逃跑王</span>
                </div>
            </div>
            <div class="player-desc">
                <p>杨佳旭，化名（旭der）绰号：无，大伙都戏称他是机灵的“小毛贼”，平日里最爱和朋友们玩闹，时不时顺手“偷走”同伴的打火机，手法娴熟，可他有个特点，得手之后立马开溜，奔跑速度一绝，堪称当之无愧的跑路王，碰到朋友间互相嬉闹打趣，他便装作视而不见，充耳不闻，安安静静当起旁观者，活泼调皮的模样十分讨喜，各式各样的小玩笑，也让彼此的相处变得热闹又有趣.
</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">92360</div>
                    <div class="text">总逃跑</div>
                </div>
                <div class="data-item">
                    <div class="num">11680</div>
                    <div class="text">逃跑成功</div>
                </div>
                <div class="data-item">
                    <div class="num">S+</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>
        <!-- 玩家卡片 7 -->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55295579538_cc995f7dc5.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>张嘉轩</h2>
                    <span class="player-tag">套狗的</span>
                </div>
            </div>
            <div class="player-desc">
                <p>张嘉轩，化名（狗王）绰号:无，大家都知道他特别会跟狗狗打交道，每次遇见小狗，他都能轻松和它们玩到一起，动作熟练又有耐心，身边人都打趣他是偷狗第一人，他为人爽朗风趣，平日里爱开玩笑，走到哪儿偷到哪，和小动物相处的十分融合，也让身边的人也偷上了狗，是个十足有趣的偷狗伙伴.
</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">666</div>
                    <div class="text">总套狗</div>
                </div>
                <div class="data-item">
                    <div class="num">667</div>
                    <div class="text">狗逃跑</div>
                </div>
                <div class="data-item">
                    <div class="num">S</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>
     <!-- 玩家卡片 8-->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55295919625_787cfe08a1.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>顾涵旭</h2>
                    <span class="player-tag">职业 | 叫妈妈</span>
                </div>
            </div>
            <div class="player-desc">
                <p>顾涵旭，化名（颗秒）绰号：无，大伙都知道他钟爱打瓦这款手游，打起游戏来格外认真，情绪也跟着战局起伏，每当局势不顺，被对手压制时，他总会脱口喊出声，这个有趣的小习惯常常逗笑身边人，他开朗直率，游戏里敢打敢拼，平日里相处也十分随和，是一起开黑玩乐的有趣伙伴.

</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">92360</div>
                    <div class="text">总叫妈</div>
                </div>
                <div class="data-item">
                    <div class="num">-250</div>                    
<div class="text">颗秒次数</div>
                </div>
                <div class="data-item">
                    <div class="num">S+</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>
      <!-- 玩家卡片 9-->
        <div class="player-card">
            <div class="line-decor"></div>
            <div class="card-head">
                <div class="avatar-box">
                    <img src="https://live.staticflickr.com/65535/55295684563_70cc7929f2.jpg" alt="玩家头像">
                </div>
                <div class="player-info">
                    <h2>顾天伦</h2>
                    <span class="player-tag">动静的神</span>
                </div>
            </div>
            <div class="player-desc">
                <p>顾天伦，化名（屁王）绰号:无，顾天伦是个活泼开朗的男生，性格大大咧咧，特别爱笑，他有一个让人忍俊不禁的小特点，平日里总爱闹出小动静，每当这时，周围的同学都会忍不住笑起来，快看他放屁了，顾天伦心胸豁达，面对大家善意的玩笑，他从不生气，还会跟着一起打趣，模样十分可爱，他待人真诚，乐于助人，平时和大家相处十分和睦，课间我们一起玩耍，聊天，有他在，教室里总是充满欢乐，这个有点小趣事.
</p>
            </div>
            <div class="player-data">
                <div class="data-item">
                    <div class="num">666</div>
                    <div class="text">总套狗</div>
                </div>
                <div class="data-item">
                    <div class="num">667</div>
                    <div class="text">狗逃跑</div>
                </div>
                <div class="data-item">
                    <div class="num">S</div>
                    <div class="text">综合评级</div>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
