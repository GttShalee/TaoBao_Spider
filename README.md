# TaoBao_Spider

这个Python脚本使用Selenium和PyQuery库，从淘宝平台爬取商品列表数据，支持根据商品关键词进行搜索，并将商品信息保存到Excel文件中。爬取的数据包括商品标题、价格、销量、地理位置、店铺信息等。

## 主要功能

- 根据关键词搜索商品
- 爬取淘宝商品列表信息
- 获取商品的详细信息，包括：
  - 商品标题
  - 商品价格
  - 销量
  - 地理位置
  - 店铺信息
  - 是否包邮
  - 商品详细链接
  - 店铺链接
  - 商品图片链接
- 将爬取的数据保存为Excel文件

## 安装依赖

本项目依赖于以下Python库：

- `selenium`: 用于控制浏览器自动化操作
- `pyquery`: 用于解析HTML和提取商品数据
- `openpyxl`: 用于操作Excel文件

### 安装命令

在开始之前，请确保已安装了以下库：

```bash
pip install selenium pyquery openpyxl
```

此外，你需要安装Chrome浏览器以及ChromeDriver，并确保其版本与Chrome浏览器匹配。你可以在[ChromeDriver官网](https://sites.google.com/a/chromium.org/chromedriver/)下载合适版本的ChromeDriver。

## 使用方法

1. **下载或克隆项目**  
   你可以通过以下命令克隆此项目：
   
   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   cd yourrepository
   ```

2. **运行脚本**  
   打开终端，进入项目目录，执行以下命令启动爬虫：
   
   ```bash
   python taobao_scraper.py
   ```

3. **输入参数**  
   脚本会要求输入以下参数：
   - **关键词（KEYWORD）**：要搜索的商品名称。
   - **爬取起始页（pageStart）**：开始爬取的页码。
   - **爬取终止页（pageEnd）**：停止爬取的页码。

   示例：
   ```bash
   输入搜索的商品关键词Keyword：手机
   输入爬取的起始页PageStart：1
   输入爬取的终止页PageEnd：5
   ```

4. **保存爬取结果**  
   脚本会根据输入的关键词生成一个包含商品信息的Excel文件，文件名格式为`<关键词>_<时间>_FromTB.xlsx`。

   示例：
   ```bash
   手机_20250410-1520_FromTB.xlsx
   ```

## 代码结构

- **taobao_scraper.py**: 主要爬虫脚本文件，包含了爬取淘宝商品信息的逻辑。
- **README.md**: 项目的说明文档。
  
## 注意事项

1. **反爬机制**：淘宝网站有一定的反爬机制，建议间隔一定时间进行爬取。如果脚本遇到验证码或其他反爬措施，请手动解决。
2. **ChromeDriver配置**：请确保安装的ChromeDriver版本与本地Chrome浏览器版本兼容。

## License

本项目遵循MIT License，详情见[LICENSE](LICENSE)文件。
