require 'cairo'
function conky_startlua()
if conky_window == nil then return end
local cs = cairo_xlib_surface_create(conky_window.display, conky_window.drawable, conky_window.visual, conky_window.width, conky_window.height)
cr = cairo_create(cs)

--координаты фона
fRoundRect (10, 10, 190, 70, 5)
local pLin = cairo_pattern_create_linear (10, 10, 190, 70) 
cairo_pattern_add_color_stop_rgba (pLin, 0.0, fRGBtoARGB(0x666666, 0.5)) 
cairo_pattern_add_color_stop_rgba (pLin, 0.4, fRGBtoARGB(0x333333, 0.5))
cairo_pattern_add_color_stop_rgba (pLin, 1, fRGBtoARGB(0x111111, 0.5))
cairo_set_source (cr, pLin)
cairo_fill(cr)
cairo_pattern_destroy (pLin)

--координаты тени виджета
fRoundRect (12, 12, 187, 67, 5)
cairo_set_line_width (cr, 5)
cairo_set_source_rgba(cr, fRGBtoARGB(0x111111, 0.05))
cairo_stroke(cr)

--координаты окантовки фона
fRoundRect (11, 11, 189, 69, 5)
cairo_set_line_width (cr, 1)
cairo_set_source_rgba(cr, fRGBtoARGB(0xffffff, 0.2))
cairo_stroke(cr)

--Виджет и условия
local nPerc = tonumber (conky_parse('${exec sh /usr/share/ya-gui/ya-calc}'))
for i = 0, 20 do

--ширина и размер шкалы
fRoundRect (173-4*i, 50, 3, 10, 2)
cairo_set_source_rgba(cr, fRGBtoARGB(0x666666, 0.8 ))

--Цвета в зависимости от условий
if i == 0 and nPerc >= 95 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 1 and nPerc >= 90 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 2 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 3 and nPerc >= 80 and nPerc < 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xffff00, 0.4)) end
if i == 3 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 4 and nPerc >= 75 and nPerc < 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xffff00, 0.4)) end
if i == 4 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 5 and nPerc >= 70 and nPerc < 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xffff00, 0.4)) end
if i == 5 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end

if i == 6 and nPerc >= 65 and nPerc < 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xffff00, 0.4)) end
if i == 6 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 7 and nPerc >= 60 and nPerc < 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xffff00, 0.4)) end
if i == 7 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 8 and nPerc >= 55 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 8 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 9 and nPerc >= 50 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 9 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 10 and nPerc >= 45 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 10 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end

if i == 11 and nPerc >= 40 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 11 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 12 and nPerc >= 35 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 12 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 13 and nPerc >= 30 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 13 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 14 and nPerc >= 25 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 14 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 15 and nPerc >= 20 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 15 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end

if i == 16 and nPerc >= 15 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 16 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 17 and nPerc >= 10 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 17 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 18 and nPerc >= 5 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 18 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 19 and nPerc >= 0 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 19 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
if i == 20 then cairo_set_source_rgba(cr, fRGBtoARGB(0x00ff00, 0.4)) end
if i == 20 and nPerc >= 85 then cairo_set_source_rgba(cr, fRGBtoARGB(0xff0000, 0.4)) end
cairo_fill(cr)
end
cairo_destroy(cr) 
end
function fRoundRect (nXCoord, nYCoord, nWidth, nHeight, nRadius)
cairo_move_to(cr, nXCoord+nRadius, nYCoord)
cairo_line_to(cr, nXCoord+nWidth-nRadius, nYCoord)
cairo_arc (cr, nXCoord+nWidth-nRadius, nYCoord+nRadius, nRadius, math.rad(270), math.rad(360))
cairo_line_to(cr, nXCoord+nWidth, nYCoord+nHeight-nRadius)
cairo_arc (cr, nXCoord+nWidth-nRadius, nYCoord+nHeight-nRadius, nRadius, math.rad(0), math.rad(90))
cairo_line_to(cr, nXCoord+nRadius, nYCoord+nHeight)
cairo_arc (cr, nXCoord+nRadius, nYCoord+nHeight-nRadius, nRadius, math.rad(90), math.rad(180))
cairo_line_to(cr, nXCoord, nYCoord+nRadius)
cairo_arc (cr, nXCoord+nRadius, nYCoord+nRadius, nRadius, math.rad(180), math.rad(270))
end
function fDrawTextCenter (nXCenter, nYCenter, sText, sFontName, sFontSize, nFontSlant, nFontWeight, nColor, nAlpha, nRotate)
local extents = cairo_text_extents_t:create()
cairo_select_font_face (cr, sFontName, nFontSlant, nFontWeight)
cairo_set_font_size (cr, sFontSize)
cairo_text_extents (cr, sText, extents)
local nXSpace = nXCenter-(extents.width/2)
local nYSpace = nYCenter
cairo_move_to (cr, nXSpace, nYSpace)
cairo_set_source_rgba(cr, fRGBtoARGB (nColor, nAlpha))
cairo_rotate (cr, nRotate*math.pi/180)
cairo_show_text(cr, sText)
cairo_rotate (cr, (0-nRotate)*math.pi/180)
end
function fRGBtoARGB (nColor, nAlpha)
return ((nColor / 0x10000) % 0x100) / 255., ((nColor / 0x100) % 0x100) / 255., (nColor % 0x100) / 255., nAlpha
end



