## ⚠️ REGRA PERMANENTE — COMANDO NÃO EXECUTADO = AVISO NA HORA (Augusto, 11/11/2026)

**Prioridade máxima. Vale para todo chat, todo projeto, toda sessão e todo agente (Claude, Claude Code, Codex, GPT) nos 19 repositórios do Augusto.**
Pedido do dono, em áudio: "Não fez o comando, me avisa. Não conseguiu fazer o comando por algum motivo, me avisa. Tá com problema de espaço na nuvem, de local, de sandbox, me avisa. Se eu fizer um comando e ele não foi executado, você tem que me avisar, seja por e-mail, seja pelo próprio aplicativo."

Motivo: em 11/11/2026 descobrimos que um pedido dele (avisos de saída e de ausência no Conexão Hair e nos grupos) **nunca foi executado e ninguém avisou**. Também havia PRs prontos parados há dias sem aviso, e testes do GitHub que nem chegavam a começar (`startup_failure`), também sem aviso.

1. **Todo pedido do dono termina em um de três estados, sempre ditos com todas as letras:** ✅ FEITO (com prova: link, PR mesclado, teste), ⏸️ PARADO (o que falta e quem precisa agir) ou ⛔ NÃO FEITO (o motivo). Silêncio não é estado.
2. **Toda resposta final tem a seção "⛔ NÃO FEITO"** quando qualquer parte do pedido ficou sem executar, mesmo que pequena. Cada item diz o quê, por quê e o que destrava.
3. **Motivos que obrigam o aviso:** falta de permissão, sandbox ou rede bloqueada, disco cheio, cobrança (GitHub Actions, Fly.io, Vercel, Supabase, Google), conector desconectado, teste que não rodou, CI que não começou, limite de uso ou de tokens, sessão interrompida, ou dúvida que ficou sem resposta.
4. **Teste que não rodou não é teste aprovado.** `startup_failure`, "pulado" ou "não deu para rodar" vai no aviso, com o que foi feito no lugar (ex.: "rodei os testes aqui na sessão").
5. **Se a sessão vai parar sem terminar** (limite, erro, bloqueio), antes de parar ela avisa pelo aplicativo (notificação push) e, quando houver conector de e-mail, por e-mail para o dono, com a lista do que ficou para trás.
6. **Rede de proteção diária:** a tarefa agendada "Rede de proteção — 19 repositórios" confere todo dia os 19 repositórios (PRs parados, branches com trabalho fora da `main`, testes vermelhos ou que não começaram, sessões bloqueadas esperando o dono) e manda o resumo por push e e-mail. Se ela falhar, isso também é aviso.
7. **Comando antigo achado sem execução** (em sessão, branch ou PR esquecido) entra no próximo aviso como ⛔ NÃO FEITO, mesmo que seja de outra sessão.
