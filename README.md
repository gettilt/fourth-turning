<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(f"# {config['name'].title()}")
]]]-->
# Fourth-Turning
<!--//[[[end]]]-->

## Mission

Tilt's mission is to map every theme to a basket of stocks for anyone to invest in. Mappings are AI generated and expert curated.
Expert improvements are accepted if they provide a better representation of a given theme.

## Theme Prompt
<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  cog.outl(config['prompt'])
]]]-->
We are in a period of crisis and upheaval, marked by societal disintegration and the breakdown of institutions. The result is war, inflation, and domestic rebuilding requiring natural resources and tech (cryptocurrency or AI.).
<!--[[[end]]]-->

## Theme Stocks

<!--[[[cog
import cog
import csv
import json

with open('context.json') as file:
  contexts = json.load(file)

def _get_context_str_for_ticker(ticker):
  try:
    context = contexts[ticker]
    context_str = context['chat_gpt'] or context['claude'] or ""
  except KeyError:
    context_str = ""

  return context_str

cog.outl("| Ticker  | Context | Source |")
cog.outl("| ------- | ---- | ---- |")

with open('theme.csv') as file:
  reader = csv.reader(file)
  next(reader) # skip the header
  for row in reader:
    context_str = _get_context_str_for_ticker(row[0])
    cog.outl(f"| {row[0]} | {context_str} | {row[1]} |")
]]]-->
| Ticker  | Context | Source |
| ------- | ---- | ---- |
| AAPL | Apple's wide range of technology products and services could see increased demand in a tech-driven rebuilding effort. | chat_gpt,claude |
| AMD | Advanced Micro Devices produces semiconductors essential for technology used in defense and rebuilding efforts. | chat_gpt,claude |
| AMZN | Amazon could benefit from increased demand for its e-commerce and cloud computing services during and after crises. | chat_gpt,claude |
| BA | Boeing could benefit from increased defense spending and the need for aircraft in both military and rebuilding efforts. | chat_gpt,google |
| BHP | BHP Group, a leading resources company, is well-positioned to supply the raw materials needed for rebuilding and defense technologies. | chat_gpt |
| CAT | Caterpillar Inc. is likely to see increased demand for its heavy machinery for rebuilding efforts in post-crisis environments. | chat_gpt,google |
| DE | Deere & Company could see increased demand for its agricultural and construction machinery in rebuilding efforts. | chat_gpt,google |
| FCX | Freeport-McMoRan, a major copper producer, stands to gain from the increased demand for copper in electronics and rebuilding. | chat_gpt,claude |
| GOOGL | Alphabet Inc. could benefit from increased demand for its AI technologies and digital services in times of rebuilding. | chat_gpt,claude,google |
| INTC | Intel Corporation's semiconductor technologies are crucial for defense, technology, and rebuilding efforts. | chat_gpt,claude |
| LMT | Lockheed Martin is a leading defense contractor, likely to benefit from increased military spending during times of war. | chat_gpt,claude,google |
| MSFT | Microsoft's cloud computing and AI technologies are essential for modern defense systems and rebuilding societal infrastructure. | chat_gpt,claude |
| NEM | Newmont Corporation, a gold mining company, could see gains as investors flock to gold as a safe haven during crises. | chat_gpt |
| NVDA | NVIDIA is at the forefront of AI technology, which is crucial for both military applications and rebuilding societal infrastructure. | chat_gpt,claude,twitter |
| PYPL | PayPal Holdings could see growth as digital payments become more prevalent in a rebuilding economy. | chat_gpt |
| RTX | Raytheon Technologies provides advanced defense and aerospace systems, which are in higher demand during conflicts. | chat_gpt,claude,google |
| SQ | Block, Inc. (formerly Square) could benefit from increased adoption of digital currencies and blockchain technology in post-crisis economies. | chat_gpt |
| TSLA | Tesla's advancements in AI and energy solutions could play a significant role in rebuilding and innovating post-crisis infrastructure. | chat_gpt,twitter |
| XOM | Exxon Mobil could benefit from increased oil prices due to geopolitical tensions affecting supply. | chat_gpt,google |
| AA |  | claude |
| CLF |  | claude |
| CRM |  | claude |
| GD |  | claude,google |
| HII |  | claude,google |
| LDOS |  | claude |
| META |  | claude |
| NOC |  | claude,google |
| NUE |  | claude,google |
| COIN |  | twitter |
| IBIT |  | twitter |
| MARA |  | twitter |
| MSTR |  | twitter |
| WULF |  | twitter |
| BIPC |  | google |
| CCI |  | google |
| FLR |  | google |
| PWR |  | google |
| VMC |  | google |
<!--[[[end]]]-->

## License

<p>
This project is licensed under <a href="./LICENSE">AGPLv3</a>.
</p>


## Contributors

Thank you for your improvements! We appreciate all the contributions from the community.

<!--[[[cog
import cog
import json
with open('config.json') as file:
  config = json.load(file)
  repo = config['github_repo'].lower()
  cog.outl(f'<a href="https://github.com/gettilt/{repo}/graphs/contributors">')
  cog.outl(f'  <img src="https://contrib.rocks/image?repo=gettilt/{repo}" />')
  cog.outl('</a>')
]]]-->
<a href="https://github.com/gettilt/fourth-turning/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=gettilt/fourth-turning" />
</a>
<!--[[[end]]]-->

## Join Our Community

<a href="https://discord.gg/4vYMhRpaMY" target="_blank">
<img src="https://discord.com/api/guilds/1179775688421683220/widget.png?style=banner3" alt="">
</a>
