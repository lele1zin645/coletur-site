# COLETUR — Landing page

## Arquivos
- `index.html` — página completa (HTML + Tailwind via CDN + JS vanilla)
- `assets/` — logotipo e fotos otimizadas

Para publicar: suba a pasta inteira (Netlify, Vercel, Hostinger). Sem build.

## Antes de publicar
1. Trocar `Sob consulta` pelos valores reais nos cards da seção `#viagens`.
2. Substituir os 3 depoimentos por depoimentos reais.
3. Conferir a data do Grenal (o card usa 03/09) e as datas do Centro Mediúnico.
4. Escrever as páginas de Termos, Privacidade e FAQ (links do rodapé estão em `#`).
5. Trocar `https://www.coletur.com.br/` no `<link rel="canonical">` pelo domínio final.

## Como adicionar um card de viagem
Copie um `<article class="card ...">` da seção `#viagens` e altere: imagem, tag colorida, data, título, descrição, valor e o texto do link do WhatsApp.

Link de reserva: `https://wa.me/5555997284701?text=` + mensagem codificada (troque espaços por `%20`, acentos por `%C3%A3` etc.).

## Chatbot
No `<script>`, o objeto `respostas` controla os botões:

```js
var respostas = {
  chave: { p: 'Texto do botão', r: 'Resposta do bot' }
};
```

Adicione ou remova chaves; os botões são gerados automaticamente. O botão verde sempre leva ao WhatsApp.

## Carrossel
Slides ficam em `#carousel` (`<div class="slide" data-slide>`). Para trocar, substitua o `<img>`. O intervalo está na constante `DELAY` (6000 ms).

## Formulários
Ambos são client-side. A busca rápida monta a mensagem e abre o WhatsApp. A newsletter apenas valida e mostra sucesso — para gravar os leads, conecte a um serviço (Formspree, Mailchimp, Brevo) no `submit` de `#newsForm`.

## Cores
Definidas em `tailwind.config` e nas variáveis CSS do `:root`: navy `#001f3f`, royal `#0074d9`, cyan `#29b6e8` (retirado do logotipo), gold `#d4af37`, silver `#e0e0e0`.
