# Signal 111 — Diário de desenvolvimento

*Atualizado em 28 de outubro de 2026*

[English](DEVELOPMENT-TRACKER-EN.md) · [Русский](DEVELOPMENT-TRACKER-RU.md) · [Español](DEVELOPMENT-TRACKER-ES.md) · [Português (Brasil)](DEVELOPMENT-TRACKER-PT-BR.md) · [简体中文](DEVELOPMENT-TRACKER-ZH-CN.md)

[Projeto](../README.md) · [Roteiro](ROADMAP.md)

## 28 de outubro — Coordenadas reais e teste com dois PCs

Consegui ler a posição e a orientação do jogador em um mundo carregado de Fallout 4 no HOST, em um teste real dentro do jogo. Depois gravei 97 amostras de movimento.

Fiz então uma tentativa com **dois computadores físicos**. O HOST enviou as 97 amostras pelo servidor e o convidado recebeu a mesma sequência e os seis valores de cada amostra, sem diferenças.

**A transferência de dados funcionou, mas a tentativa completa falhou.** Houve um marcador de desconexão inválido no convidado e, depois, um tempo limite no HOST. Ainda não existem dois personagens no mesmo mundo.

Reproduzi e corrigi um problema na publicação do marcador de diagnóstico. A correção passou nos testes offline, mas **ainda não foi testada novamente com dois PCs**.

Também preparei um módulo de diagnóstico para criar, observar e remover um Actor local. A compilação e as verificações offline passaram. **O módulo ainda não foi carregado no jogo.**

## 26 de outubro — Preparando o teste no mundo

Preparei a leitura protegida das coordenadas e continuei estudando a segurança dos saves. Naquele momento, os resultados ainda eram offline.

## 25 de outubro — Duas identidades de rede

Dois clientes reais de Fallout 4 se conectaram ao mesmo servidor e receberam identidades de rede diferentes. Ambos permaneceram nos menus.

## 24 de outubro — Duas conexões

Verifiquei duas conexões simultâneas e um acesso básico aos dados do jogador no menu.

## Próximos passos

Verificar a segurança dos perfis de teste, a desconexão entre dois PCs e um Actor local antes de avançar para personagens remotos.

**Ainda não existe uma versão cooperativa jogável.**

[Changelog](../CHANGELOG.md) · [Tarefas](https://github.com/PawPaw228/Fallout-Together-Signal_111/issues)
