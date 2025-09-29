# 📝 Como usar o script de adicionar Moedas Visuais no Sala do Futuro

## 1. Crie o favorito (bookmarklet)
- Copie o código do script (aquele que começa com `javascript:(function(){...})();`).
- No navegador, adicione um **novo favorito**.
- No campo **URL/endereço**, cole o código inteiro.
- No campo **Nome**, coloque algo como:  
  `🪙 Moedas Adicionais`

## 2. Acesse sua conta
- Entre normalmente no site do **Sala do Futuro**.
- Faça login com sua conta.

## 3. Navegue até o site da Árvore 
- Clique em **Árvore**.  
- Depois vá em **Plantações**.  

## 4. Execute o script
- Clique no favorito **🪙 Moedas Adicionais**.  

## 5. Coleta final
- Verifique se seu saldo Mudou
- Pronto**.

---

## 📦 Código do Script

```javascript
javascript:(function(){var spans=document.querySelectorAll("span");var nums=[];spans.forEach(function(s){var txt=s.textContent.trim();if(/^\d+$/.test(txt)){nums.push(s);}});if(nums.length===0){alert("Nenhum n%C3%BAmero em <span> encontrado");return;}nums.forEach(function(s){var v=parseInt(s.textContent.trim(),10)||0;s.textContent=v+500;});})();
