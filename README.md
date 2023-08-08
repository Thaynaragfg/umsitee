# umsitee
import turtle

# Função para desenhar a bola
def draw_ball(x, y):
    turtle.penup()
    turtle.goto(x, y)
    turtle.pendown()
    turtle.circle(20)

# Função para fazer a bola rolar na tela
def ball_rolling():
    x = -180
    y = 0
    for _ in range(200):
        turtle.clear()
        draw_ball(x, y)
        y -= 2  # Movimento vertical da bola
        x += 2  # Movimento horizontal da bola
        turtle.update()

# Configuração da tela
turtle.setup(400, 400)
turtle.bgcolor("white")
turtle.title("Bola Rolando")
turtle.tracer(0)

# Desenhar a bola na posição inicial
draw_ball(-180, 0)
turtle.update()

# Fazer a bola rolar na tela
ball_rolling()

turtle.done()
