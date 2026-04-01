# XISBE

# Guia de Contribuição: Fork, Commits e Sincronização

Este guia explica passo a passo como podes contribuir para este repositório de forma segura utilizando o fluxo de *Fork* e *Pull Request* (PR), e como manteres a tua cópia atualizada com o repositório original.

---

## Fazer o Fork do Repositório
O *Fork* cria uma cópia exata deste repositório na tua própria conta do GitHub, permitindo-te fazer alterações sem afetar o projeto original.

1. No canto superior direito da página do repositório, clica no botão **Fork**.
2. Escolhe a tua conta do GitHub como destino.
3. Agora tens uma cópia do projeto em `github.com/TEU-USER/NOME-DO-REPO`.

---

## Clonar o teu Fork para o Computador
Agora precisas de trazer a tua cópia (o fork) para a tua máquina local para começares a trabalhar.

Abre o terminal e executa:
```bash
git clone [https://github.com/TEU-USER/NOME-DO-REPO.git](https://github.com/TEU-USER/NOME-DO-REPO.git)
cd NOME-DO-REPO
```

---

## Contribuir (Fazer as tuas alterações)
É uma boa prática nunca trabalhar diretamente na branch `main`. Cria sempre uma nova branch para a tua funcionalidade ou correção.

**1. Criar uma nova branch:**
```bash
git checkout -b minha-nova-funcionalidade
```

**2. Fazer o teu trabalho:**
Edita os ficheiros, escreve o teu código e guarda as alterações.

**3. Registar as alterações (Commit):**
```bash
git add .
git commit -m "feat: adiciona nova funcionalidade X"
```

**4. Enviar para o teu GitHub (Push):**
```bash
git push origin minha-nova-funcionalidade
```

---

## Criar um Pull Request (PR)
Agora que as tuas alterações estão no teu GitHub, tens de pedir para as integrarmos no repositório original.

1. Vai à página do teu repositório (o teu fork) no GitHub.
2. Vais ver um aviso verde a dizer **Compare & pull request**. Clica aí.
3. Escreve um título claro e uma descrição do que alteraste.
4. Clica em **Create pull request**.
5. Está feito! Agora é só esperar que os administradores do projeto revejam o teu código.

---

## Manter o teu Fork Atualizado
Enquanto trabalhas, o repositório original pode receber novas atualizações de outras pessoas. Para garantires que o teu código não fica desatualizado (evitando conflitos), tens de sincronizar o teu fork.

### Método 1: Pelo site do GitHub (O mais fácil)
1. Vai à página principal do teu fork no GitHub.
2. Clica no botão **Sync fork** (mesmo abaixo do botão verde *Code*).
3. Clica em **Update branch**. O teu fork está agora sincronizado! No teu computador, basta fazeres `git pull origin main`.

### Método 2: Pela Linha de Comandos (Terminal)
Caso prefiras fazer tudo pelo terminal, tens de ligar o teu repositório local ao repositório original (chamado de `upstream`).

**1. Adicionar o repositório original (só precisas de fazer isto uma vez):**
```bash
git remote add upstream [https://github.com/USER-ORIGINAL/NOME-DO-REPO.git](https://github.com/USER-ORIGINAL/NOME-DO-REPO.git)
```

**2. Sincronizar as novidades:**
Sempre que quiseres atualizar a tua cópia, executa:
```bash
git fetch upstream
git checkout main
git merge upstream/main
git push origin main
```
