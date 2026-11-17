# 管道分县施工进度的公开回执采集 RPA

现有项目保存县区申请与服务回执的冻结响应。transport 核对请求与字节来源，domain 提取资料身份，ledger 原子保存原文与版本，view 呈现已接收资料及缺口。合成样例不访问真实站点；业务关联和完整性判断尚未实现。

Python 3.11 以上，在项目根目录执行：

    python -m unittest discover -s tests -v
    python -m compileall -q capture_service tests
    python -m capture_service.cli inspect data/normal.json

Docker 构建和运行：docker build -t hydrogen-collection-005 .；docker run --rm hydrogen-collection-005。
