---
layout: default
title: JSONC
---

# Tools and Libraries

Several tools and libraries support JSONC, enabling developers to parse and generate JSONC data easily. This is a non-exhaustive list organized by programming language.

## Parsers

| Language   | Tool/Library                                      | Comments | Trailing Commas | Notes                          |
|----------- |---------------------------------------------------|----------|-----------------|--------------------------------|
| C          | [jmtilli/caj][CAJ]                                | 🟡 [^1]  | 🟡 [^2]        |                                |
| C++        | [nlohmann/json][nlohmann]                         | 🟡 [^3]  | 🟡 [^4]        |                                |
| C++        | [RapidJSON][rapidjson]                            | 🟡 [^5]  | 🟡 [^6]        |                                |
| C++        | [stephenberry/glaze][glaze]                       | 🟢 [^7]  | 🔴             |                                |
| Elixir     | [massivefermion/jsonc][massivefermion]            | 🟢       | 🟢             | Includes additional extensions |
| Go         | [HuJSON][hujson]                                  | 🟢       | 🟢             |                                |
| Go         | [tidwall/jsonc][tidwall]                          | 🟢       | 🟢             |                                |
| Java       | [Jackson][Jackson]                                | 🟡 [^8]  | 🟡 [^9]        |                                |
| JavaScript | [microsoft/node-jsonc-parser][msft]               | 🟢       | 🟡 [^10]       |                                |
| Kotlin     | [kotlinx.serialization.json][kotlinx]             | 🟡 [^11] | 🟡 [^12]       |                                |
| PHP        | [otar/jsonc][otar]                                | 🟢       | 🟢             |                                |
| Python     | [n-takumasa/json-with-comments][n-takumasa]       | 🟢       | 🟢             |                                |
| Rust       | [dprint/jsonc-parser][dprint]                     | 🟢       | 🟢             |                                |
| Swift      | [steelbrain/JSONCKit][steelbrain]                 | 🟢       | 🟢             |                                |

Legend:

🟢: Default support <br>
🟡: Optional support <br>
🔴: Unsupported <br>

[otar]: https://github.com/otar/jsonc
[steelbrain]: https://github.com/steelbrain/JSONCKit
[hujson]: https://github.com/tailscale/hujson
[rapidjson]: https://github.com/Tencent/rapidjson
[nlohmann]: https://github.com/nlohmann/json
[CAJ]: https://github.com/jmtilli/caj
[glaze]: https://github.com/stephenberry/glaze
[tidwall]: https://github.com/tidwall/jsonc
[Jackson]: https://github.com/FasterXML/jackson-core
[massivefermion]: https://github.com/massivefermion/jsonc
[msft]: https://github.com/microsoft/node-jsonc-parser
[kotlinx]: https://kotlinlang.org/api/kotlinx.serialization/kotlinx-serialization-json/
[n-takumasa]: https://github.com/n-takumasa/json-with-comments
[dprint]: https://github.com/dprint/jsonc-parser

<hr>

[^1]: Use `caj_allow_comments(ctx)`

[^2]: Use `caj_allow_trailing_comma(ctx)`

[^3]: Use `ignore_comments`

[^4]: Use `ignore_trailing_commas`

[^5]: Use `kParseCommentsFlag`

[^6]: Use `kParseTrailingCommasFlag`

[^7]: Use `glz::read_jsonc` (or using options: `glz::opts{.comments = true}`). See [Documentation](https://github.com/stephenberry/glaze/blob/main/docs/json.md#json-with-comments-jsonc).

[^8]: Use `JsonFactory.enable(JsonReadFeature.ALLOW_JAVA_COMMENTS)`

[^9]: Use `JsonFactory.enable(JsonReadFeature.ALLOW_TRAILING_COMMA)`

[^10]: Use `allowTrailingComma: true`

[^11]: Use `allowComments`. See [Documentation](https://kotlinlang.org/api/kotlinx.serialization/kotlinx-serialization-json/kotlinx.serialization.json/-json-builder/allow-comments.html).

[^12]: Use `allowTrailingComma`. See [Documentation](https://kotlinlang.org/api/kotlinx.serialization/kotlinx-serialization-json/kotlinx.serialization.json/-json-builder/allow-trailing-comma.html).
