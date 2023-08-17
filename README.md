- 👋 Hi, I’m @santiamancops34
- 👀 I’m interested inpygame.init()

# Colores
NEGRO = (0, 0, 0)
VERDE = (
VERDE =
0, 255, 0)
ROJO = (255, 0, 0)

# Tamaño de la pantalla
ANCHO = 800
ALTO = 
AL
600

# Tamaño de los bloques
TAMANO_BLOQUE = 
TAMANO_BLOQUE =
20

# Inicialización de la pantalla
pantalla = pygame.display.set_mode((ANCHO, ALTO))
pygame.display.set_caption("Clebrita")

# Reloj para controlar la velocidad de actualización
reloj = pygame.time.Clock()


re
def dibujar_clebrita(clebrita):
    for segmento in clebrita:
        pygame.draw.rect(pantalla, VERDE, (segmento[
        pygame.draw.rect(pantalla, VERDE, (
0], segmento[1], TAMANO_BLOQUE, TAMANO_BLOQUE))

def main():
    # Posición inicial de la serpiente
    cabeza_x = ANCHO // 2
    cabeza_y = ALTO // 
    cabeza_y =

    cabeza
2

    # Velocidad inicial
    velocidad_x = 0
    velocidad_y = 0

    # Lista para almacenar la serpiente
    clebrita = [(cabeza_x, cabeza_y)]

    
   
# Posición aleatoria de la comida
    comida_x = random.randrange(
    comida_x =
0, ANCHO - TAMANO_BLOQUE, TAMANO_BLOQUE)
    comida_y = random.randrange(
    comida
0, ALTO - TAMANO_BLOQUE, TAMANO_BLOQUE)

    while True:
        for evento in pygame.event.get():
            if evento.type == pygame.QUIT:
                pygame.quit()
                quit()

            # Captura las teclas presionadas para controlar la dirección de la serpiente
            if evento.type == pygame.KEYDOWN:
                if evento.key == pygame.K_UP:
                    velocidad_x = 0
                    velocidad_y = -TAMANO_BLOQUE
                
                    velocidad_y =

                    velocidad
elif evento.key == pygame.K_DOWN:
                    velocidad_x = 0
                    velocidad_y = TAMANO_BLOQUE
                
                    velocidad_y = TAMANO_BLOQUE
               
elif evento.key == pygame.K_LEFT:
                    velocidad_x = -TAMANO_BLOQUE
                    velocidad_y = 
                    velocidad
0
                elif evento.key == pygame.K_RIGHT:
                    velocidad_x = TAMANO_BLOQUE
                    velocidad_y = 
                    velocidad_x = TAMANO
0

        

# Actualiza la posición de la serpiente
        cabeza_x += velocidad_x
        cabeza_y += velocidad_y

        
        cabeza_x += velocidad_x
        cabeza_y += velocidad_y
# Actualiza la lista de la serpiente
        clebrita.append((cabeza_x, cabeza_y))

        # Si la cabeza de la serpiente alcanza la posición de la comida, genera una nueva posición aleatoria para la comida
        if cabeza_x == comida_x and cabeza_y == comida_y:
            comida_x = random.randrange(
            comida_x = random
0, ANCHO - TAMANO_BLOQUE, TAMANO_BLOQUE)
            comida_y = random.randrange(0, ALTO - TAMANO_BLOQUE, TAMANO_BLOQUE)
        
       
else:
            # Si no se comió la comida, elimina el último segmento de la serpiente para que parezca que está avanzando
            clebrita.pop(
           
0)

        

# Dibuja la serpiente y la comida en la pantalla
        pantalla.fill(NEGRO)
        dibujar_clebrita(clebrita)
        pygame.draw.rect(pantalla, ROJO, (comida_x, comida_y, TAMANO_BLOQUE, TAMANO_BLOQUE))

        pygame.display.update()
        reloj.tick(10)  # Controla la velocidad de actualización

if __name__ == "__main__":
    main()
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
santiamancops34/santiamancops34 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
