🐋 Ambiente Laravel + Docker (Windows)

Este repositório contém uma arquitetura base para rodar projetos Laravel utilizando Docker no Windows, sem precisar instalar PHP, Composer, MySQL ou qualquer outra tecnologia diretamente na sua máquina.
Tudo roda dentro de containers Docker, garantindo desempenho, organização e fácil manutenção. 🚀

⚙️ Como funciona

O Docker cria um ambiente isolado chamado container, onde ficam todos os serviços que o Laravel precisa (PHP, MySQL, Nginx, etc).
No caso deste projeto:

O Windows compartilha o diretório do projeto com o Docker, ou seja:
tudo que você alterar nos arquivos do projeto no Windows é refletido automaticamente dentro do container.

Apesar disso, nenhum serviço está instalado no seu Windows — tudo é executado dentro do Docker.

Isso evita problemas de versões, conflitos de instalação e lentidão no sistema.
Se quiser remover o ambiente, basta parar e apagar os containers, sem deixar rastros no computador.

🧱 Benefícios dessa arquitetura

✅ Sem bagunça no Windows: nada de instalações manuais de PHP, Composer, MySQL etc.
✅ Ambiente padronizado: todos os desenvolvedores usam a mesma versão de cada serviço.
✅ Fácil de remover e reinstalar: se algo der errado, basta remover os containers e subir novamente.
✅ Flexibilidade total: você pode trabalhar com várias versões de tecnologias ao mesmo tempo (ex: MySQL 5.7 e MySQL 8.0, PHP 7.4 e PHP 8.2, etc).
✅ Independência: não depende de WAMP, XAMPP ou outros servidores locais.

🪄 Como iniciar o projeto

Instale o Docker Desktop (para Windows 10 ou superior).
👉 https://www.docker.com/products/docker-desktop

Clone o repositório:

git clone https://github.com/seu-usuario/nome-do-repo.git
cd nome-do-repo


Suba os containers:

docker-compose up -d


Acesse o projeto:

http://localhost

🧰 Estrutura principal
📦 seu-projeto/
 ┣ 📁 laravel/            # Código-fonte do Laravel
 ┣ 📁 docker/             # Configurações dos containers
 ┣ 📄 docker-compose.yml  # Arquitetura dos serviços
 ┗ 📄 README.md           # Este arquivo :)

💬 Explicando de forma simples

Pense no Docker como uma “máquina virtual leve” que roda dentro do seu Windows.
Ela cria “caixinhas” (containers) independentes para cada tecnologia, por exemplo:

Uma caixinha para o PHP

Uma caixinha para o MySQL

Uma caixinha para o Nginx

Tudo conversa entre si dentro do Docker, mas sem tocar no seu sistema Windows diretamente.
E se você quiser limpar tudo, basta apagar as caixinhas — seu Windows continua limpinho e sem registros sobrando.

🧑‍💻 Ideal para

Iniciantes em Laravel e Docker

Devs que querem um ambiente pronto e padronizado

Equipes que buscam evitar “funciona na minha máquina”

Quem quer rodar várias versões de projetos no mesmo computador sem conflitos

❤️ Contribuindo

Este é um projeto público — sinta-se à vontade para abrir issues, enviar melhorias ou compartilhar ideias!
Toda contribuição é bem-vinda. 🤝
