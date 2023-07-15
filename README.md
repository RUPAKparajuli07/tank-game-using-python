"""
Tanks Game Documentation
Author: Rupak Parajuli

This program is a simple tank shooting game implemented using the Pygame library.

Dependencies:
- Pygame

Classes:
- None

Functions:
- Score(score)
- txt_object(txt, color, size="small")
- txt_btn(message, color, btnx, btny, btnwidth, btnheight, size="vsmall")
- msg_screen(message, color, y_displace=0, size="small")
- tank(x, y, turret_position)
- computer_tank(x, y, turret_position)
- game_ctrls()
- btn(txt, x, y, width, height, inactive_color, active_color, action=None, size=" ")
- pause()
- barrier(x_loc, ran_height, bar_width)
- explosion(x, y, size=50)
- playerfireShell(xy, tankx, tanky, turPost, gun_power, xloc, bar_width, ranHeight, eTankX, eTankY)
- computerfireShell(xy, tankx, tanky, turPost, gun_power, xloc, bar_width, ranHeight, ptankx, ptanky)
- power(level)
- game_intro()
- game_over()
- you_win()
- health_bars(p_health, e_health)
- gameLoop()

Constants:
- display_width: The width of the game display in pixels.
- display_height: The height of the game display in pixels.
- game_layout_display: The Pygame display surface object.
- Resources: The loaded image resource for the game background.
- wheat, white, black, blue, red, light_red, yellow, light_yellow, green, light_green: Color constants.
- clock: The Pygame Clock object.
- tnk_width: The width of the tank in pixels.
- tnk_height: The height of the tank in pixels.
- tur_width: The width of the tank turret in pixels.
- whl_width: The width of the tank wheels in pixels.
- grnd_height: The height of the ground in pixels.
- s_font, m_font, l_font, vs_font: Pygame Font objects for different sizes.
- gun: The current tank turret position.
- gExit: Boolean variable to control the game loop exit condition.
- gOver: Boolean variable to track if the game is over.
- FPS: Frames per second for the game loop.
- p_health: Player's health.
- e_health: Enemy's health.
- bar_width: The width of the barrier in pixels.
- mTankX: Player's tank x-coordinate.
- mTankY: Player's tank y-coordinate.
- tnkMove: The tank's horizontal movement.
- curTurPost: The current tank turret position.
- changeTurs: Change in turret position.
- eTankX: Enemy tank x-coordinate.
- eTankY: Enemy tank y-coordinate.
- f_power: The power of the shot.
- p_change: Change in power.
- xloc: The x-coordinate of the barrier.
- ranHeight: The height of the barrier.

Functions Documentation:

1. Score(score)
    - Description: Displays the score on the game layout display.
    - Parameters:
        - score (int): The current score.
    - Returns: None

2. txt_object(txt, color, size="small")
    - Description: Returns a tuple containing the rendered text surface and its rectangle object.
    - Parameters:
        - txt (str): The text to be rendered.
        - color (tuple): The color of the text in RGB format.
        - size (str, optional): The size of the text. Defaults to "small".
    - Returns: (pygame.Surface, pygame.Rect)

3. txt_btn(message, color, btnx, btny, btnwidth, btnheight, size="vsmall")
    - Description: Renders and displays a text button on the game layout display.
    - Parameters:
        - message (str): The text to be displayed on the button.
        - color (tuple): The color of the text in RGB format.
        - btnx (int): The x-coordinate of the button.
        - btny (int): The y-coordinate of the button.
        - btnwidth (int): The width of the button.
        - btnheight (int): The height of the button.
        - size (str, optional): The size of the text. Defaults to "vsmall".
    - Returns: None

4. msg_screen(message, color, y_displace=0, size="small")
    - Description: Displays a message on the game layout display.
    - Parameters:
        - message (str): The message to be displayed.
        - color (tuple): The color of the text in RGB format.
        - y_displace (int, optional): The displacement of the message in the y-direction. Defaults to 0.
        - size (str, optional): The size of the text. Defaults to "small".
    - Returns: None

5. tank(x, y, turret_position)
    - Description: Draws and displays the player's tank on the game layout display.
    - Parameters:
        - x (int): The x-coordinate of the tank.
        - y (int): The y-coordinate of the tank.
        - turret_position (int): The position of the tank's turret.
    - Returns: The position of the tank's turret.

6. computer_tank(x, y, turret_position)
    - Description: Draws and displays the enemy's tank on the game layout display.
    - Parameters:
        - x (int): The x-coordinate of the tank.
        - y (int): The y-coordinate of the tank.
        - turret_position (int): The position of the tank's turret.
    - Returns: The position of the tank's turret.

7. game_ctrls()
    - Description: Displays the game controls screen and handles user input.
    - Parameters: None
    - Returns: None

8. btn(txt, x, y, width, height, inactive_color, active_color, action=None, size=" ")
    - Description: Renders and displays a button on the game layout display and handles button actions.
    - Parameters:
        - txt (str): The text to be displayed on the button.
        - x (int): The x-coordinate of the button.
        - y (int): The y-coordinate of the button.
        - width (int): The width of the button.
        - height (int): The height of the button.
        - inactive_color (tuple): The color of the button when inactive in RGB format.
        - active_color (tuple): The color of the button when active in RGB format.
        - action (str, optional): The action to be performed when the button is clicked. Defaults to None.
        - size (str, optional): The size of the text. Defaults to " ".
    - Returns: None

9. pause()
    - Description: Pauses the game and handles user input to continue playing or quit the game.
    - Parameters: None
    - Returns: None

10. barrier(x_loc, ran_height, bar_width)
    - Description: Draws and displays a barrier on the game layout display.
    - Parameters:
        - x_loc (int): The x-coordinate of the barrier.
        - ran_height (int): The height of the barrier.
        - bar_width (int): The
