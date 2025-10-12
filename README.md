# Joel Souza - Site Profissional

Template HTML profissional para desenvolvedor com deploy automático via GitHub Actions.

## 🚀 Deploy Automático

Este projeto está configurado para fazer deploy automático para HostGator usando GitHub Actions.

### Configuração dos Secrets

Para que o deploy funcione, você precisa configurar os seguintes secrets no GitHub:

1. Acesse o repositório no GitHub
2. Vá em **Settings** → **Secrets and variables** → **Actions**
3. Clique em **New repository secret** e adicione:

#### `FTP_HOST`
- **Valor**: O hostname do seu servidor FTP da HostGator
- **Exemplo**: `ftp.joelsouza.com.br` ou `ftp.hostgator.com`
- **Como encontrar**: No painel da HostGator, vá em "FTP Accounts" ou "File Manager"

#### `FTP_USER`
- **Valor**: Seu usuário FTP
- **Exemplo**: `joelsouza@joelsouza.com.br` ou apenas `joelsouza`
- **Como encontrar**: No painel da HostGator, em "FTP Accounts"

#### `FTP_PASS`
- **Valor**: Sua senha FTP
- **Exemplo**: `sua_senha_aqui`
- **Como encontrar**: No painel da HostGator, em "FTP Accounts"

### Informações Comuns da HostGator

- **Servidor FTP**: Geralmente `ftp.seudominio.com.br`
- **Porta**: 21 (padrão)
- **Protocolo**: FTP (não SFTP)
- **Diretório**: `public_html/` (onde ficam os arquivos do site)

### Como Testar a Conexão

Antes de configurar o GitHub Actions, teste a conexão FTP:

1. Use um cliente FTP como FileZilla
2. Conecte com as mesmas credenciais que você vai usar nos secrets
3. Verifique se consegue acessar a pasta `public_html/`

### Troubleshooting

#### Erro "ENOTFOUND ***"
Este erro indica que o DNS não consegue resolver o hostname do servidor FTP.

**Soluções:**
1. **Verifique se os secrets estão configurados:**
   - Vá em Settings → Secrets and variables → Actions
   - Confirme que `FTP_HOST`, `FTP_USER` e `FTP_PASS` existem

2. **Teste a conectividade:**
   ```bash
   ping ftp.joelsouza.com.br
   telnet ftp.joelsouza.com.br 21
   ```

3. **Verifique o hostname correto:**
   - No painel da HostGator, vá em "FTP Accounts"
   - Use o servidor FTP exato mostrado lá
   - Geralmente é `ftp.seudominio.com.br`

4. **Teste com cliente FTP primeiro:**
   - Use FileZilla ou similar
   - Conecte com as mesmas credenciais
   - Se não conectar, o problema é nas credenciais

#### Erro de Autenticação
- Verifique se `FTP_USER` e `FTP_PASS` estão corretos
- Teste as credenciais em um cliente FTP primeiro
- Certifique-se de que não há espaços extras nos secrets

#### Erro de Permissão
- Certifique-se de que o usuário FTP tem permissão para escrever na pasta `joelsouza/`
- Verifique se a conta FTP está ativa no painel da HostGator
- Confirme que o diretório de destino existe no servidor

## 📁 Estrutura do Projeto

```
joelsouza.com.br/
├── index.html          # Página principal
├── styles.css          # Estilos CSS
├── script.js           # JavaScript
├── .github/
│   └── workflows/
│       └── deploy.yml  # Configuração do deploy
└── README.md           # Este arquivo
```

## 🎨 Personalização

Para personalizar o site:

1. **Informações pessoais**: Edite o `index.html`
2. **Cores e estilos**: Modifique o `styles.css`
3. **Funcionalidades**: Ajuste o `script.js`
4. **Foto de perfil**: Substitua o ícone por uma imagem real

## 📱 Recursos

- ✅ Design responsivo
- ✅ Navegação suave
- ✅ Animações CSS/JS
- ✅ Formulário de contato
- ✅ Deploy automático
- ✅ SEO otimizado

## 🔧 Tecnologias

- HTML5
- CSS3
- JavaScript (Vanilla)
- GitHub Actions
- FTP Deploy Action
