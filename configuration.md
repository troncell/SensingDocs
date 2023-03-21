# 文档配置
## 文档配置地址
> /Retail/config.json

## 文档配置文件结构
-- retail                   零售
    -- name                 分类名
    -- data                 零售中包含的子类
        -- title            子类名
        -- icon             子类的icon
            -- greyIcon     子类未选中时icon
            -- lightIcon    子类选中时icon
            -- w            icon宽度
            -- h            icon高度
        -- path             子类路由（注：与文档所在文件名保持一致）
        -- pages            子类中所包含的文档分类
            -- id           文档分类id
            -- title        文档分类标题
            -- url          文档地址数组
                -- name     文档名称 
            -- type         文档分类中文档类型（注：multiple为多文档，single为单文档，单文档时无需写数组）
-- showroom                 展厅
-- factory                  工厂
-- downloadCenter           下载中心

注：文档中若使用本地图片，图片路径写到根目录；例如：/Docs/Sample/images/H5images/2.png
    <img style="width:100px" class="right" src="/Docs/Sample/images/H5images/2.png" alt="H5images" />

文档存放再Docs目录下且文件名首字母大写