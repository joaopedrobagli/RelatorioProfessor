<template>
    <div>
      <!-- Defina sua biblioteca de mensagens aqui -->
      <div ref="BibliotecaMensagens">
        <div v-for="(section, sectionName) in messages" :key="sectionName">
          <div v-for="(message, code) in section" :key="code">
            {{ code }}: {{ message }}
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        messages: {
          conta_perfil: {
            alterar_senha: "Alterou a senha do perfil.",
            alterar_foto: "Alterou a foto do perfil.",
            alterar_dados: "Alterou dados cadastrais do perfil.",
            alterar_email: "Alterou e-mail do perfil.",
            alterar_cpf: "Atualizou o CPF para %usuario-cpf%.",
            gerar_senha: "Gerou senha de acesso.",
            remover_dispositivo:
              "Removeu o dispositivo conectado a conta. Dispositivo %device-id% - %device-nome%.",
            associar_google:
              "Associou a conta google %conta-google% em seu perfil na plataforma.",
            associar_apple:
              "Associou a conta apple %conta-apple% em seu perfil na plataforma.",
            associar_microsoft:
              "Associou a conta microsoft %conta-microsoft% em seu perfil na plataforma.",
            desassociar_google:
              "Desassociou a conta google %conta-google% em seu perfil na plataforma.",
            desassociar_apple:
              "Desassociou a conta apple %conta-apple% em seu perfil na plataforma.",
            desassociar_microsoft:
              "Desassociou a conta microsoft %conta-microsoft% em seu perfil na plataforma."
          },
          conta_acesso: {
            sair: "Desconectou-se da plataforma.",
            padrao: "Conectou-se na plataforma com usuário e senha.",
            memorizado: "Conectou-se na plataforma com login memorizado.",
            microsoft: "Conectou-se na plataforma pela conta microsoft %conta-microsoft%.",
            google: "Conectou-se na plataforma pela conta google %conta-google%.",
            apple: "Conectou-se na plataforma pela conta apple %conta-apple%."
          },
          conta_cadastro: {
            padrao: "Criou uma conta na plataforma com cadastro padrão.",
            microsoft: "Criou uma conta na plataforma com o login microsoft %conta-microsoft%.",
            google: "Criou uma conta na plataforma com o login google %conta-google%.",
            apple: "Criou uma conta na plataforma com o login apple %conta-apple%."
          },
          conta_recuperar: {
            solicitar: "Solicitou recuperação da conta por e-mail.",
            redefinir_senha: "Redefiniu senha de acesso."
          },
          conta_seguranca: {
            ativar_2fa: "Ativou autenticação de 2 fatores.",
            atualizar_2fa: "Atualizou a autenticação de 2 fatores.",
            validar_2fa: "Validou autenticação de 2 fatores."
          }
        }
      };
    }

  };
  </script>
  