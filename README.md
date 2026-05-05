# Raymarching-Experiments
J'ai voulu tester de reproduire des effets visuel codé avec des shaders nottament pour creer des objets 3D,
des effets visuel comme de la lumière réaliste, de la diffusion lumineuse, du [Raymarching](https://fr.wikipedia.org/wiki/Ray_marching), raytracing....

Ici les projets utilisent du Raymarching qui est une technique consotant a projeter des rayons depuis la 
camera jusqu'à trouver une surface mais sans connaitre la position de la surface.

Le projet se compose de plusieurs sous projets qui sont créé avec [ShaderToy](https://www.shadertoy.com/)
Les shaders sont des scripts qui sont executé pour chacun des pixels de l'écran, executé par la carte graphique
en parallèle.

# Sphere with Raymarching
Ce projet est une simple sphere et un plane éclairé par une lumière qui se deplace.
La technique ici consiste à tirer des rayons depuis une caméra et à voir quand il arrive a une certaine distance 
d'un objet, a ce moment on considère le pixel comme valide et on peut afficher une couleur. (Raymarching)


Après l'affichage de la couleur on peut calculer la lumiere:

$$
L = \hat{n} \cdot \hat{l}
$$


$$
L = \int_0^D T(t)\cdot\sigma_s \cdot L_{\text{in}}(t)\space dt \approx \sum_{i} T_i \cdot \sigma_s \cdot\Delta t\cdot L_{\text{in}}(p_i)
$$
