# Taxcalendario::Client

Client da API do Taxweb Calendario.

## Instalação

Adicione a linha a seguir no seu Gemfile:

```ruby
gem 'calendario-gem'
```

A seguir, execute:

    $ bundle install

Ou instale manualmente com o comando:

    $ gem install calendario-gem

## Exemplo de uso

```ruby
require 'taxcalendario/client'

user_api = Taxcalendario::Client::UserService.new
user_api.access_token = "COLOQUE_AQUI_SEU_TOKEN"
user_api.contas.each do |conta|
    puts conta.nome
end
```

## Documentação

O RDoc se encontra no diretório "doc". Lá é possível ver todas as classes clientes e suas entidades.

## Testes

Para executar os testes, copie o arquivo spec/test_template.yml para spec/test.yml e execute rspec.
Execute os testes em um DUMP de producao. Como a API nao possui rotinas administrativas, estabelecimentos com entregas e obrigacoes, sao necessarios para a execucao.

