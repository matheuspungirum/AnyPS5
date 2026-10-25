# Sobre

> 🇧🇷 **Português (BR)** · [🇺🇸 English version below](#about)

Ferramenta para portar executáveis automaticamente para Linux e Windows.

A build apenas do relinker roda no macOS, incluindo Apple silicon.

[**Conversor web**](https://boykopovar.github.io/AnyPS5/) - os arquivos ficam no seu dispositivo.

![anyps5_collage1](https://github.com/user-attachments/assets/ed2f0b2d-33d3-46d7-ab88-767ca872fc99)

Inclui um [relinker](core/relinker) que converte o executável para o formato nativo do sistema de destino e implementações das [bibliotecas prx do sistema](core/libs/prx) adequadas para linkagem dinâmica. Sem emulação e sem processo de runtime separado.

[**Discord**](https://discord.gg/BHFztBPUe), [Uso](docs/user/USAGE.md), [Instruções de build](docs/dev/BUILD.md), [Arquitetura](docs/dev/ARCHITECTURE.md), [Débito técnico do projeto](docs/dev/TechnicalDebt.md), [convenções de estilo de código](docs/dev/CONVENTIONS.md), [como contribuir](CONTRIBUTING.md)

## Status

[![libraries](https://boykopovar.github.io/AnyPS5/badge-libraries.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![shaders](https://boykopovar.github.io/AnyPS5/badge-shaders.svg)](https://boykopovar.github.io/AnyPS5/progress.html)

[![mapa de progresso](https://boykopovar.github.io/AnyPS5/progress.svg)](https://boykopovar.github.io/AnyPS5/progress.html)

[Histórico de progresso](https://boykopovar.github.io/AnyPS5/history.html)

<sub>* Bibliotecas do sistema: percentual das funções conhecidas pelo projeto até agora (declaradas em [core/libs/prx](core/libs/prx)), e não de todas as funções do sistema do PS5. O total cresce à medida que mais funções são declaradas.</sub>

Estados não suportados ou inesperados lançam estritamente `std::runtime_error`. O `what()` é impresso no stderr e o processo é encerrado.

O [recompilador de shaders](core/shader/recompiler/Recompiler.cpp) gera SPIR-V com sucesso (validado via [Spirv-Tools](3rdparty/SPIRV-Tools) quando compilado com `ANYPS5_ENABLE_SPIRV_TOOLS`).

## Compatibilidade

O progresso por jogo (etapa alcançada, bloqueios em aberto, cobertura de bibliotecas e de GPU) é acompanhado no [mapa de bloqueios](https://alxcbtw.github.io/anyps5-roadmap/), um projeto da comunidade construído a partir de dados públicos do GitHub ([código-fonte](https://github.com/AlxcBTW/anyps5-roadmap)). Relatórios de teste vão nas discussões de [Game bring-up](https://github.com/boykopovar/AnyPS5/discussions/categories/game-bring-up), um tópico por título.

## Mapeamento de controles

Controles mapeados via SDL são suportados, incluindo analógicos e gatilhos. Teclado e mouse podem ser configurados com um arquivo `anyps5-input.ini`. Veja [mapeamento de controles](docs/user/INPUT_MAPPING.md) para os dispositivos suportados e o formato de configuração.

## Aviso legal

Este projeto destina-se a fins de interoperabilidade, pesquisa, preservação e compatibilidade. Ele não inclui, distribui nem exige software, firmware, chaves criptográficas ou bibliotecas proprietárias protegidos por direitos autorais. Os usuários são responsáveis por garantir que quaisquer binários usados com este projeto sejam obtidos e utilizados de acordo com as leis aplicáveis e os respectivos termos de licença.

O AnyPS5 é um projeto independente e não é afiliado, autorizado ou endossado pela Sony Interactive Entertainment. "PlayStation" e "PS5" são marcas registradas da Sony Interactive Entertainment Inc.

## Licença

Este projeto é licenciado sob a GNU General Public License, versão 2 apenas.

---

# About

> 🇺🇸 **English (original)** · [🇧🇷 Versão em português acima](#sobre)

Tool for automatic executables porting to Linux and Windows.

The relinker-only build runs on macOS, including Apple silicon.

[**Web converter**](https://boykopovar.github.io/AnyPS5/) - files stay on your device.

![anyps5_collage1](https://github.com/user-attachments/assets/ed2f0b2d-33d3-46d7-ab88-767ca872fc99)

Includes a [relinker](core/relinker) that converts executable to the target system's native format and implementations of [system prx libraries](core/libs/prx) suitable for dynamic linking. No emulation or separate runtime process.

[**Discord**](https://discord.gg/BHFztBPUe), [Usage](docs/user/USAGE.md), [Build instructions](docs/dev/BUILD.md), [Architecture](docs/dev/ARCHITECTURE.md), [Technical debt of the project](docs/dev/TechnicalDebt.md), [code style conventions](docs/dev/CONVENTIONS.md), [contributing](CONTRIBUTING.md)

## Status

[![libraries](https://boykopovar.github.io/AnyPS5/badge-libraries.svg)](https://boykopovar.github.io/AnyPS5/progress.html) [![shaders](https://boykopovar.github.io/AnyPS5/badge-shaders.svg)](https://boykopovar.github.io/AnyPS5/progress.html)

[![progress map](https://boykopovar.github.io/AnyPS5/progress.svg)](https://boykopovar.github.io/AnyPS5/progress.html)

[Progress history](https://boykopovar.github.io/AnyPS5/history.html)

<sub>* System libraries: percentage of the functions known to the project so far (declared in [core/libs/prx](core/libs/prx)), not of every PS5 system function. The total grows as more functions are declared.</sub>

Unsupported or unexpected states strictly throw `std::runtime_error`. `what()` is printed to stderr and the process terminates.

The [shader recompiler](core/shader/recompiler/Recompiler.cpp) successfully produces SPIR-V (validated via [Spirv-Tools](3rdparty/SPIRV-Tools) when built with `ANYPS5_ENABLE_SPIRV_TOOLS`).

## Compatibility

Per-game progress (stage reached, open blockers, libraries and GPU coverage) is tracked on the [blocker map](https://alxcbtw.github.io/anyps5-roadmap/), a community project built from public GitHub data ([source](https://github.com/AlxcBTW/anyps5-roadmap)). Test reports go in the [Game bring-up](https://github.com/boykopovar/AnyPS5/discussions/categories/game-bring-up) discussions, one thread per title.

## Input mapping

SDL-mapped game controllers are supported, including analog sticks and triggers. Keyboard and mouse controls can be configured with an `anyps5-input.ini` file. See [input mapping](docs/user/INPUT_MAPPING.md) for the supported devices and configuration format.

## Disclaimer

This project is intended for interoperability, research, preservation, and compatibility purposes. It does not include, distribute, or require copyrighted software, firmware, cryptographic keys, or proprietary libraries. Users are responsible for ensuring that any binaries used with this project are obtained and used in accordance with applicable laws and their respective license terms.

AnyPS5 is an independent project and is not affiliated with, authorized or endorsed by Sony Interactive Entertainment. "PlayStation" and "PS5" are trademarks of Sony Interactive Entertainment Inc.

## License

This project is licensed under the GNU General Public License version 2 only.
