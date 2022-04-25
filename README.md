# tugas-QL-grup5

##  RL 18 April 2022
Sebagai syarat untuk memenuhi tugas RL 18 April 2022 </br>
Kelompok :
  1. M. Azis pangestu, Khasanah Ilmi, 1051914
  2. Aisyah Sekar Ayu Dzikron, Khasanah Ilmi, 1908667
  3. Ari Fitria, Khasanah Ilmi, G74180014
  4. Rahmatul Fajri, Khasanah Ilmi, 180120201035
  5. Hernando Dio Palma, Khasanah Ilmi, 3332190049.

## Tugas :
  - Merubah tata letak environtment yang sudah ada, mulai dari posisi robot, posisi goal yang dituju dan tata letak obstacle. Dirubah bagian env.py

### Perbandingan Sebelum dan Sesudah Modifikasi
| ![map1.png](https://user-images.githubusercontent.com/28534765/165027959-5bd329b9-cac3-4a3d-859c-0a700ff24c79.png) |
|:--:|
| <b>Posisi rintangan sebelum dimodifikasi</b>|

| ![image](https://user-images.githubusercontent.com/28534765/165029134-9c33d8bc-e447-489c-9fb2-7a1d7da978f7.png) |
|:--:|
| <b>Rute Terdekat Sebelum Dimodifikasi</b>|

| ![map2.png](https://user-images.githubusercontent.com/28534765/165028052-23250041-b2ee-482e-b2a5-39e3a0cb757e.png) |
|:--:|
| <b>Posisi rintangan setelah dimodifikasi</b>|

| ![image](https://user-images.githubusercontent.com/28534765/165029200-91f4d8b2-8a6a-4e0b-9a04-daa210721eb0.png) |
|:--:|
| <b>Rute Terdekat Setelah Dimodifikasi</b>|

| ![graph1.png](https://user-images.githubusercontent.com/28534765/165028851-70984bf0-cba8-4b68-a9df-b3386ed092a0.png) |
|:--:|
| <b>Grafik Episode dan Cost Sebelum Dimodifikasi</b>|

| ![graph2](https://user-images.githubusercontent.com/28534765/165029009-6f2cfec6-3ed0-48ce-ac32-ef44f8e5949c.png) |
|:--:|
| <b>Grafik Episode dan Cost Setelah Dimodifikasi</b>|

### Bagian Kode yang sudah dimodifikasi
        # Obstacles from 1 to 22
        self.obstacle1 = self.canvas_widget.create_image(pixels * 5, 0, anchor='nw', image=self.obstacle11_object)
        # Obstacle 2
        self.obstacle2 = self.canvas_widget.create_image(0, pixels * 1, anchor='nw', image=self.obstacle4_object)
        # Obstacle 3
        self.obstacle3 = self.canvas_widget.create_image(pixels * 2, pixels * 1, anchor='nw', image=self.obstacle1_object)
        # Obstacle 4
        self.obstacle4 = self.canvas_widget.create_image(pixels * 7, pixels * 1, anchor='nw', image=self.obstacle2_object)
        # Obstacle 5
        self.obstacle5 = self.canvas_widget.create_image(pixels * 4, pixels * 2, anchor='nw', image=self.obstacle9_object)
        # Obstacle 6
        self.obstacle6 = self.canvas_widget.create_image(0, pixels * 3, anchor='nw', image=self.obstacle9_object)
        # Obstacle 7
        self.obstacle7 = self.canvas_widget.create_image(pixels * 5, pixels * 3, anchor='nw', image=self.obstacle3_object)
        # Obstacle 8
        self.obstacle8 = self.canvas_widget.create_image(pixels * 6, pixels * 3, anchor='nw', image=self.obstacle2_object)
        # Obstacle 9
        self.obstacle9 = self.canvas_widget.create_image(pixels * 7, pixels * 3, anchor='nw', image=self.obstacle6_object)
        # Obstacle 10
        self.obstacle10 = self.canvas_widget.create_image(pixels * 2, pixels * 4, anchor='nw', image=self.obstacle8_object)
        # Obstacle 11
        self.obstacle11 = self.canvas_widget.create_image(pixels * 3, pixels * 4, anchor='nw', image=self.obstacle10_object)
        # Obstacle 12
        self.obstacle12 = self.canvas_widget.create_image(pixels * 5, pixels * 4, anchor='nw', image=self.obstacle5_object)
        # Obstacle 13
        self.obstacle13 = self.canvas_widget.create_image(0, pixels * 5, anchor='nw', image=self.obstacle9_object)
        # Obstacle 14
        self.obstacle14 = self.canvas_widget.create_image(pixels * 5, pixels * 5, anchor='nw', image=self.obstacle3_object)
        # Obstacle 15
        self.obstacle15 = self.canvas_widget.create_image(pixels * 6, pixels * 5, anchor='nw', image=self.obstacle2_object)
        # Obstacle 16
        self.obstacle16 = self.canvas_widget.create_image(pixels * 7, pixels * 5, anchor='nw', image=self.obstacle6_object)
        # Obstacle 17
        self.obstacle17 = self.canvas_widget.create_image(pixels * 4, pixels * 6, anchor='nw', image=self.obstacle9_object)
        # Obstacle 18
        self.obstacle18 = self.canvas_widget.create_image(0, pixels * 7, anchor='nw', image=self.obstacle4_object)
        # Obstacle 19
        self.obstacle19 = self.canvas_widget.create_image(pixels * 2, pixels * 7, anchor='nw', image=self.obstacle1_object)
        # Obstacle 20
        self.obstacle20 = self.canvas_widget.create_image(pixels * 7, pixels * 7, anchor='nw', image=self.obstacle7_object)
        # Obstacle 21
        self.obstacle21 = self.canvas_widget.create_image(pixels * 5, pixels * 8, anchor='nw', image=self.obstacle12_object)
        # Obstacle 22
        #self.obstacle22 = self.canvas_widget.create_image(pixels * 2, pixels * 3, anchor='nw', image=self.obstacle2_object)

        # Final Point
        img_flag = Image.open("images/flag.png")
        self.flag_object = ImageTk.PhotoImage(img_flag)
        self.flag = self.canvas_widget.create_image(pixels * 6, pixels * 4, anchor='nw', image=self.flag_object)

        # Uploading the image of Mobile Robot
        img_robot = Image.open("images/agent1.png")
        self.robot = ImageTk.PhotoImage(img_robot)

        # Creating an agent with photo of Mobile Robot
        self.agent = self.canvas_widget.create_image(0, pixels * 4, anchor='nw', image=self.robot)

        # Packing everything
        self.canvas_widget.pack()
