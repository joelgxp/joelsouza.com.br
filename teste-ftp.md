# Teste de Conectividade FTP

## Como testar se o servidor FTP está acessível:

### 1. Teste com ping (no terminal):
```bash
ping ftp.joelsouza.com.br
# ou
ping ftp.hostgator.com
```

### 2. Teste com telnet:
```bash
telnet ftp.joelsouza.com.br 21
```

### 3. Teste com cliente FTP:
- Use FileZilla, WinSCP ou similar
- Conecte com as mesmas credenciais que você vai usar nos secrets

## Informações Comuns da HostGator:

### Para domínio próprio (joelsouza.com.br):
- **Servidor**: `ftp.joelsouza.com.br`
- **Usuário**: `joelsouza@joelsouza.com.br` ou apenas `joelsouza`
- **Senha**: Sua senha FTP
- **Porta**: 21
- **Diretório**: `public_html/` ou `joelsouza/`

### Para subdomínio HostGator:
- **Servidor**: `ftp.hostgator.com`
- **Usuário**: `joelsouza@joelsouza.com.br`
- **Senha**: Sua senha FTP
- **Porta**: 21
- **Diretório**: `public_html/`

## Checklist de Verificação:

- [ ] O domínio `joelsouza.com.br` está ativo?
- [ ] O FTP está habilitado no painel da HostGator?
- [ ] As credenciais FTP estão corretas?
- [ ] O servidor FTP responde ao ping?
- [ ] Os secrets estão configurados no GitHub?

## Comandos para Testar:

### Windows (PowerShell):
```powershell
Test-NetConnection ftp.joelsouza.com.br -Port 21
```

### Linux/Mac:
```bash
nc -zv ftp.joelsouza.com.br 21
```

## Se nada funcionar:

1. **Verifique no painel da HostGator:**
   - Vá em "FTP Accounts"
   - Confirme o servidor FTP correto
   - Teste a conexão pelo painel

2. **Entre em contato com o suporte da HostGator:**
   - Peça para verificar se o FTP está funcionando
   - Confirme as credenciais corretas
   - Verifique se há bloqueios de firewall
