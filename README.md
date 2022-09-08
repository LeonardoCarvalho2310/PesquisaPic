# PesquisaPic
Repositório de um projeto de automação para criação de usuário em um site.

describe ('Login e registro de usuários alura pic', () => {

    beforeEach(() => {
        cy.visit('https://alura-fotos.herokuapp.com');
    })

it('verifica mensagens validacao', () => {
    cy.contains('a','Register now').click();
    cy.contains('button', 'Register').click();
    cy.contains('ap-vmessage', 'Email is required').should('be.visible');
    cy.contains('button', 'Register').click();
    cy.contains('ap-vmessage', 'Full name is required').should('be.visible');
    cy.contains('ap-vmessage', 'Password is required').should('be.visible');
    cy.contains('ap-vmessage', 'User name is required').should('be.visible');

    })


})
