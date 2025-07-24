# KoboldGame

Здесь я буду выкладывать код написанный на питоне.
Игра будет наипростейшей и глупой, так что ожидать что-то крутое не стоит

А вот и сам код:
\
\
\
import pygame

pygame.init()

screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("Kobold Walker")


icon = pygame.image.load('images/icon.png')
pygame.display.set_icon(icon)


bg = pygame.image.load('images/SPOILER_IMG_430.jpg')


walk_right = [
    pygame.image.load('images/player/Stay on the right.png'),
    pygame.image.load('images/player/Walk on the right.png')
]

player_anim_count = 0
animation_speed = 10

running = True
clock = pygame.time.Clock()

while running:

    screen.blit(bg, (0, 0))
    screen.blit(walk_right[player_anim_count], (470, 300))


    player_anim_count = (player_anim_count + 1) % len(walk_right)

    pygame.display.update()
    clock.tick(animation_speed)

pygame.quit()
