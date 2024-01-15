ss run program 
![image](https://github.com/tiarahasnabila/game/assets/127285118/384d1cbb-ea35-45fc-b1a0-c58fe4cd4466)
![image](https://github.com/tiarahasnabila/game/assets/127285118/592229d1-87b0-4116-874d-1f3eefa4650f)

ss program
![code](https://github.com/tiarahasnabila/game/assets/127285118/41b9579f-4018-4956-ac4e-757049eff730)

Metode dalam class GameObject(object):
__init__(self, canvas, item):untuk menginisialisasi objek GameObject.
get_position(self): untuk mendapatkan posisi saat ini objek
move(self, x, y): untuk memindahkan objek di atas kanvas 
delete(self): untuk menghapus objek dari kanvas.

Metode dalam class Ball(GameObject):
__init__(self, canvas, x, y): untuk menginisialisasi objek Ball.
update(self): memperbarui posisi bola
collide(self, game_objects): menangani tabrakan bola dengan objek game lain

Metode dalam class Paddle(GameObject):
__init__(self, canvas, x, y): untuk menginisialisasi objek Paddle.
set_ball(self, ball): untuk mengasosiasikan bola dengan paddle.
move(self, offset): untuk memindahkan paddle di atas kanvas

Metode dalam class Brick(GameObject):
__init__(self, canvas, x, y, hits): untuk menginisialisasi objek Brick.
hit(self): untuk menangani ketika brick terkena

Metode dalam class Game(tk.Frame):
__init__(self, master):untuk menginisialisasi permainan.
restart_game(self): untuk memulai ulang permainan dengan set baru 
setup_game(self): untuk menyiapkan kondisi awal permainan dengan bola 
toggle_pause(self): untuk menjeda atau melanjutkan permainan dan menampilkan pesan "Paused".
add_ball(self): untuk menambahkan bola baru ke permainan.
add_brick(self, x, y, hits): untuk menambahkan brick baru ke permainan.
draw_text(self, x, y, text, size='40'): untuk menggambar teks di atas kanvas.
update_lives_text(self): untuk memperbarui tampilan jumlah lives.
start_game(self):untuk memulai loop permainan setelah pemain memulai permainan.
game_loop(self): untuk loop permainan yang menangani tabrakan
check_collisions(self): untuk memeriksa tabrakan antara bola dan objek permainan lainnya.
