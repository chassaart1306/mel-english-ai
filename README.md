# Mel English — Emma AI

Aplicativo web de conversação em inglês com uma professora virtual, voltado à comunicação profissional internacional. A integração usa a API da OpenAI e exige uma chave própria com faturamento habilitado.

## Iniciar localmente

1. Instale Node.js 18 ou superior.
2. Abra um terminal nesta pasta.
3. Configure a chave de API **no servidor**, nunca no HTML:
   - macOS/Linux: `export OPENAI_API_KEY='sua-chave'`
   - Windows PowerShell: `$env:OPENAI_API_KEY='sua-chave'`
4. Execute `node server.js`.
5. Abra `http://localhost:3000`.

Opcional: defina `OPENAI_MODEL=gpt-4o-mini` ou outro modelo compatível com chat completions e JSON mode.

## Publicar para a Mel

Hospede este projeto em um serviço Node.js com HTTPS, como Render ou Railway. Configure `OPENAI_API_KEY` como variável de ambiente privada no painel do serviço, comando inicial `node server.js` e porta atribuída pelo provedor. Nunca publique a chave no repositório. Para um site público, adicione autenticação, limites por usuário e controles de gastos antes de distribuir o link.

## Limitações

- A IA conversa e corrige texto transcrito, mas não avalia a pronúncia acusticamente.
- A voz de Emma usa síntese de voz do navegador; a qualidade depende do dispositivo.
- O reconhecimento de voz depende do navegador, da permissão de microfone e de HTTPS em produção.
- A chave de API e a hospedagem são necessárias para a IA funcionar. A API pode gerar custos de uso.
- Não armazena histórico no servidor. O histórico curto é mantido apenas na página enquanto ela estiver aberta.
- A página `pratica-guiada.html` mantém a versão anterior para prática sem IA.
