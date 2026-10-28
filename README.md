# Alliance Salto

Site institucional estático da Alliance Salto, feito em HTML, CSS e JavaScript sem etapa de build. As imagens locais ficam em `assets/`.

## Publicação no GitHub + EasyPanel

1. Envie este repositório para o GitHub.
2. No EasyPanel, crie um serviço do tipo **App** e conecte o repositório.
3. Selecione **Dockerfile** como método de build e use a raiz do repositório como contexto.
4. Configure a porta interna como **80** e publique o domínio desejado com HTTPS.
5. Faça o deploy. O EasyPanel servirá `index.html` e usará `404.html` para rotas inexistentes.

O Dockerfile usa Nginx Alpine e não exige variáveis de ambiente nem compilação.

## Teste local opcional

```sh
docker build -t alliance-salto .
docker run --rm -p 8080:80 alliance-salto
```

Acesse `http://localhost:8080`.
