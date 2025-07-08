# boost.vcpkg

Este pacote NuGet fornece a biblioteca **Boost** (versão conforme especificado no pacote), compilada com o [vcpkg](https://github.com/microsoft/vcpkg) para **Windows x64** usando o **Microsoft Visual Studio 2022 (toolset v143)**.

## 📦 Conteúdo do pacote

- Arquivos de cabeçalho (`include/boost/*.hpp`, `.h`)
- Bibliotecas estáticas e/ou dinâmicas (`.lib` e `.dll`) para os módulos Boost selecionados
- Arquivo `.targets` que configura automaticamente:
  - Include paths
  - Lib paths
  - Dependências
  - Cópia dos `.dll` para a pasta de saída (se aplicável)

## ⚙️ Como usar

1. Adicione o pacote ao seu projeto C++ via NuGet.

2. O Visual Studio aplicará automaticamente as configurações via o arquivo `.targets` incluído.

3. Certifique-se de que o projeto esteja em plataforma **x64**.

## 🔁 Configuração automática

- As bibliotecas Boost necessárias são linkadas automaticamente conforme o modo (Debug/Release).
- As DLLs (se houver) são copiadas para `$(OutDir)` após o build.

## 📝 Licença

- **Boost**: [Boost Software License 1.0](https://www.boost.org/users/license.html)
- Este pacote NuGet: [Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)

## 🔗 Links úteis

- Site oficial: https://www.boost.org/
- Fonte: https://github.com/boostorg/boost
- vcpkg: https://github.com/microsoft/vcpkg
