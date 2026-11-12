# Tela Compartilhada

Transmita a tela do seu PC para amigos direto pelo navegador, ponto a ponto (WebRTC), sem servidor próprio.

**Abrir:** https://murilobraz.github.io/tela-compartilhada/

---

## Tirar o som do Discord da transmissão

Ao compartilhar a **tela inteira** com "Compartilhar áudio", o navegador captura tudo que toca no
**dispositivo de saída padrão** do Windows, incluindo a chamada do Discord. Por isso quem assiste se
ouve de volta. O navegador não permite excluir um programa, então a solução é fazer o Discord tocar
por outro caminho.

**Ideia:** o padrão do Windows vira um cabo virtual (é isso que vai para a transmissão), você escuta
esse cabo no seu fone, e o Discord toca **direto no fone**, sem passar pelo cabo.

```
Jogos, YouTube, apps ─► CABLE Input (padrão) ─► transmissão ✅
                              └─► "Ouvir este dispositivo" ─► seu fone
Discord ─────────────────────────────────────────► seu fone (não vai para a transmissão) 🚫
```

### 1. Instale o VB-CABLE (gratuito)
1. Baixe em **https://vb-audio.com/Cable/**
2. Extraia o zip, clique com o botão direito em `VBCABLE_Setup_x64.exe` e escolha **Executar como administrador**, depois **Install Driver**.
3. Reinicie o PC.

### 2. Deixe o cabo como saída padrão
**Configurações → Sistema → Som → Saída** e escolha **CABLE Input (VB-Audio Virtual Cable)**.

### 3. Continue ouvindo tudo no seu fone
1. **Configurações → Sistema → Som → Mais configurações de som** (abre o painel clássico)
2. Aba **Gravação**, depois **CABLE Output**, **Propriedades** e a aba **Escutar**
3. Marque **Ouvir este dispositivo** e, em "Reproduzir por este dispositivo", escolha **seu fone ou caixa de som**
4. Clique em **OK**

### 4. Mande o Discord direto para o fone
No Discord: **Configurações de usuário → Voz e vídeo → Dispositivo de saída** e escolha **seu fone
pelo nome**. Não use "Padrão", senão ele volta para o cabo.

### 5. Teste
Comece uma transmissão com **tela inteira** e **Compartilhar áudio do sistema** marcado. Na janela do
app, o som de um vídeo deve chegar aos amigos, mas a chamada do Discord não.

### Para desfazer
Volte a saída padrão do Windows para o seu fone e desmarque **Ouvir este dispositivo** no CABLE Output.

### Alternativa sem instalar nada
Compartilhe uma **aba do navegador** em vez da tela inteira. Só o som daquela aba é transmitido.
