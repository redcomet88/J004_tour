# J004 vue+springboot 旅游推荐算法情感分析|spark+bilstm情感分析+景点协同过滤推荐+百度地图Echarts可视化分析|管理端增删改查|数据大屏

> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从git来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 
关注B站，有好处！
编号:  J004
## 视频

[video(video-tFGCDLtc-1757378086364)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=618529099)(image-https://i-blog.csdnimg.cn/img_convert/976a8dc34d95fd7745297efa3a5a2ca3.jpeg)(title-最强旅游大数据vue+springboot 百度地图集成路线规划、门票购买、协同过滤推荐算法、回归客流预测算法、spark、最强源码)]

## 1 系统简介
Vue + Spring Boot 旅游推荐可视化系统”是一个功能比较完善的旅游平台，它不仅提供了用户端的旅游景点浏览和个性化推荐功能（基于UserCF和ItemCF），还具备强大的后台管理能力，方便管理员维护旅游内容和用户。更重要的是，系统通过“可视化”和“数据大屏”模块，将各类运营数据和旅游数据以直观、美观的方式呈现出来，这对于分析系统运营情况、用户行为以及旅游热点和趋势都非常有价值。技术栈上采用Vue.js和Spring Boot，是当前流行的前后端分离架构，有利于开发效率和系统扩展性。。
## 2 功能设计
本旅游推荐可视化系统采用经典的前后端分离架构设计，以提供高效、可扩展且用户体验良好的应用。用户通过浏览器作为客户端访问系统，浏览器负责渲染由 Vue前端 提供的用户界面（UI）。Vue前端基于HTML、CSS、JavaScript，并利用Vuex管理全局状态、Vue Router实现页面路由，Echarts组件则用于构建丰富的可视化数据图表，从而呈现主页、旅游推荐、可视化分析等功能。前端通过异步通信（如Ajax）与 Spring Boot后端 进行数据交互。Spring Boot后端作为业务逻辑层，负责处理前端请求，包括旅游推荐算法（UserCF/ItemCF）、数据查询、管理操作等，并通过 MyBatis-Plus 框架简化ORM操作，高效地对底层 MySQL数据库 进行数据访问和持久化，存储并管理所有旅游相关数据（如用户、景点、线路、订单等）。这种分层设计确保了系统的模块化、高内聚低耦合，便于开发、部署和维护。
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7ba661587d694dbeb8a77dc7120d2ee2.png)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0c6c6f91d19f4255973acfa561be5f38.png)
### 2.3 部署文档 
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f899d438164043faa72d8e245963593a.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1f9f11368baf4923931d28e4027d3bab.png)
### 2.4 项目目录
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a3828f851a5d4ccf8a009e1b18765797.png)

## 3 网站 功能展示
### 3.1 登录 & 注册
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/eedf752b7dfd463dabd46142ec8dcf5c.png)
### 3.2 主页 & 数据统计
提供网站的整体数据概览和统计信息，可能包括用5A、4A景区、公园、水世界等，让用户对网站运营状况有所了解。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5100cb09eb82461fa4c1d098f0716246.png)

### 3.3 推荐算法
这是系统的核心功能之一。利用用户协同过滤 (UserCF) 和 物品协同过滤 (ItemCF) 算法为用户推荐旅游景点。
- UserCF (基于用户的协同过滤): 根据与当前用户兴趣相似的其他用户的偏好来推荐旅游景点。
- ItemCF (基于物品的协同过滤): 根据用户之前喜欢过的音乐找到与其相似的其他旅游景点进行推荐。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/19b19bda9eab4982bd4eeeba5d8d8c2d.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0b4bdfedbe5143a9a9b12ea97aebcb05.png)
### 3.4 可视化分析
- 景区热度分析: 以图表等可视化方式展示景区热度趋势等。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/df44d9af466e475695abcfaf930d9880.png)
- 景区分布分析: 利用中国地图方式可视化展示景区分布趋势等。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d67c7635f7b045599b0f3a2d8ff2092a.png)

- 景区地点分析: 利用花瓣图、柱状图方式可视化展示景区地点趋势等。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/340ab96a239d46c08887b7db1dde1592.png)
### 3.5 词云分析
词云分析: 对进行文本分析，生成词云图，直观展示中高频出现的关键词，帮助用户快速了解景区的关键词。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/865843d1f525434cac9aff21dfd93d87.png)
### 3.6 修改密码
提供用户更改密码的功能。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0b9ddcc6d1934331ba95ae8a34d3d120.png)
### 3.7 数据查询
允许用户根据关键词、等条件查询景区信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/1f6fcf3c292b4b93b7d714b7756c7039.png)
### 3.8 个人中心
**会员办理**：通过支付宝沙箱技术实现模拟支付，完成办理会员业务。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/5d02f45015444cc99ba9bed630c10987.png)
**实名认证**：通过上传身份证自动识别姓名、身份证等信息，点击完成实名认证。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b9ea92fd39554cb0b9dbd973073f9d42.png)
### 3.9 详情页面
### 3.9.1 详细信息
实现评分控件、百度地图控件和热度水滴图、下方还时间了带情感分析接口的评论区。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/a488916b33ed443b8397c8deedbb52bb.png)
### 3.9.2 评分
通过评分控件实现对 的评分，评分是0~5分
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/cee0bbb377f847edae2f6a242bd1b59d.png)
### 3.9.3 评论
通过**LSTM技术**对用户的评论进行情感分析，给出好评或者差评的分类结果。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/7905bb6e50ac4732969df3a72d17f7b4.png)
### 3.9.4 地图标注
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f6267e6c0d6347d0a08a4ed5d6c573bc.png)
### 3.10 浏览历史
用户浏览历史会记录，在浏览历史菜单下可以查看到。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/09cc5fe7035347889b46a2490b331b19.png)

## 4 管理系统 功能展示
### 4.1 登录 
该模块主要面向系统管理员，用于对网站内容、用户和数据进行管理和维护。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/9a8aca9b1c3349b6824a0004a2e3063d.png)
### 4.2 主页
查看目前系统运行情况的统计，还可以通过图形分析目前用户的来源【饼图】，以及用户性别【柱状图图】
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/97af443ba0e14dcface69c63ec478e04.png)
### 4.3 管理个人信息
用户可以自行管理和修改个人资料，如昵称、头像、密码等。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/de0b8fa8f5df455792d75fcb7231a19f.png)
### 4.4 权限
 对系统用的权限进行管理
 ![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fbfb6a2450f94f469db0da91c2ccc394.png)
### 4.5 用户管理
对系统用户进行管理。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/72bb5d9afaf14133bb99e2e809956808.png)
### 4.6 景点管理
 对景点信息进行管理，包括景点名称、图片、简介、级别、地点等。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/716b12bcc5704f9893e0a9212348428e.png)
### 4.7 评论管理
管理用户对景区的评论，包括审核、删除违规评论等。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/04bfed3c970e40abbe129e269cbcd8c1.png)
## 5 可视化大屏 功能展示
### 5.1 数据大屏

该大屏基于Vue、Spring Boot和MySQL架构，并以ECharts技术实现数据可视化，进行了全面的旅游大数据分析，主要聚焦于用户行为、消费数据、景点数据和地理分布。

具体分析包括：

用户行为分析： 通过用户登录情况（次数、趋势）、用户来源地域（省份占比）和金主充值占比，揭示用户活跃度、地域分布和消费能力。
消费与订单分析： 对交易笔数、交易金额进行时间轴分析，展示消费趋势。同时，订单总额、用户职业和性别占比也提供了用户画像的深度信息。
景点数据分析与销量分析： 通过词云展示热门关键词，热点数据分析（如价格和销量）揭示景点受欢迎程度。5A、4A景区销量则展示了不同等级景区的市场表现。
热门城市与热力图： 通过柱状图展示热门旅游城市，并结合热力图可视化用户分布和热门区域，为旅游线路规划和市场推广提供地理层面的洞察。
这些分析帮助运营者全面了解用户，优化产品和营销策略，提升用户体验和业务效益。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2530359ee9dc4582bf7a4cbe433e259d.png)
## 6 程序代码
### 6.1 代码说明
代码介绍：该算法基于协同过滤（Collaborative Filtering）实现旅游景点推荐。算法首先通过皮尔逊相关系数计算用户之间的相似度，然后根据相似用户的评分数据生成推荐列表。具体步骤包括：
数据加载：加载用户-景点评分矩阵。
相似度计算：使用皮尔逊相关系数计算用户之间的相似度。
推荐生成：根据相似用户的评分数据，为目标用户生成推荐列表。 该算法能够有效捕捉用户行为模式，提供个性化的旅游推荐服务。
### 6.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0ea9ecdf35884a27b4ac3353f5873364.png)
### 6.3 代码实例
```java
import java.util.*;
import java.util.stream.Collectors;

public class TouristAttractionRecommender {
    private Map<String, Map<String, Double>> userRatingMap; // 用户-景点评分矩阵
    private List<String> allAttractions; // 所有景点列表

    public TouristAttractionRecommender(Map<String, Map<String, Double>> userRatingMap) {
        this.userRatingMap = userRatingMap;
        this.allAttractions = userRatingMap.values().stream()
                .map(Map::keySet)
                .flatMap(Set::stream)
                .distinct()
                .collect(Collectors.toList());
    }

    /**
     * 计算用户之间的相似度（皮尔逊相关系数）
     */
    private double calculateSimilarity(String user1, String user2) {
        List<Double> ratings1 = new ArrayList<>();
        List<Double> ratings2 = new ArrayList<>();
        for (String attraction : allAttractions) {
            if (userRatingMap.get(user1).containsKey(attraction)) {
                ratings1.add(userRatingMap.get(user1).get(attraction));
            } else {
                ratings1.add(0.0);
            }
            if (userRatingMap.get(user2).containsKey(attraction)) {
                ratings2.add(userRatingMap.get(user2).get(attraction));
            } else {
                ratings2.add(0.0);
            }
        }
        // 计算协方差和标准差
        double covariance = 0.0;
        double stdDev1 = 0.0;
        double stdDev2 = 0.0;
        for (int i = 0; i < ratings1.size(); i++) {
            covariance += (ratings1.get(i) - 3) * (ratings2.get(i) - 3);
            stdDev1 += Math.pow(ratings1.get(i) - 3, 2);
            stdDev2 += Math.pow(ratings2.get(i) - 3, 2);
        }
        stdDev1 = Math.sqrt(stdDev1);
        stdDev2 = Math.sqrt(stdDev2);
        if (stdDev1 == 0 || stdDev2 == 0) {
            return 0.0;
        }
        return covariance / (stdDev1 * stdDev2);
    }

    /**
     * 为目标用户生成推荐列表
     */
    public List<String> recommend(String targetUser, int topN) {
        Map<String, Double> similarityMap = new HashMap<>();
        for (String user : userRatingMap.keySet()) {
            if (!user.equals(targetUser)) {
                double similarity = calculateSimilarity(targetUser, user);
                similarityMap.put(user, similarity);
            }
        }
        // 根据相似度排序
        List<Map.Entry<String, Double>> sortedUsers = similarityMap.entrySet().stream()
                .sorted((e1, e2) -> e2.getValue().compareTo(e1.getValue()))
                .collect(Collectors.toList());

        Set<String> recommendedAttractions = new HashSet<>();
        for (Map.Entry<String, Double> entry : sortedUsers) {
            String similarUser = entry.getKey();
            for (Map.Entry<String, Double> ratingEntry : userRatingMap.get(similarUser).entrySet()) {
                String attraction = ratingEntry.getKey();
                if (!userRatingMap.get(targetUser).containsKey(attraction) && ratingEntry.getValue() > 3) {
                    recommendedAttractions.add(attraction);
                    if (recommendedAttractions.size() >= topN) {
                        break;
                    }
                }
            }
        }
        return new ArrayList<>(recommendedAttractions).stream()
                .limit(topN)
                .collect(Collectors.toList());
    }

    public static void main(String[] args) {
        // 示例数据
        Map<String, Map<String, Double>> userRatingMap = new HashMap<>();
        userRatingMap.put("user1", Map.of("attraction1", 4.0, "attraction2", 3.0));
        userRatingMap.put("user2", Map.of("attraction1", 3.0, "attraction3", 4.0));
        userRatingMap.put("user3", Map.of("attraction2", 4.0, "attraction3", 5.0));

        TouristAttractionRecommender recommender = new TouristAttractionRecommender(userRatingMap);
        List<String> recommendations = recommender.recommend("user1", 2);
        System.out.println("推荐的景点： " + recommendations);
    }
}

```
