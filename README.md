# dwm no mouse operation

This patch is to support the operation experience without mouse intervention on dwm.

# Feature

- Window float switch
- Window move
- Window resize
- Mouse click
- Mouse move
- Mouse move - quick

# Usage

You should patch [0001-dwm-no-mouse-operation.patch](https://github.com/fengwk/dwm-no-mouse-operation/blob/main/0001-dwm-no-mouse-operation.patch).

By default the following keys are used to control the mouse, you can modify them at will:

```
/* 窗口控制 */
{ Mod4Mask,                     XK_f,         togglefloating,  {0} },              // 窗口浮动开关
{ Mod4Mask,                     XK_Up,        movewin,         {.ui = WIN_UP} },       // 向上移动窗口
{ Mod4Mask,                     XK_Down,      movewin,         {.ui = WIN_DOWN} },     // 向下移动窗口
{ Mod4Mask,                     XK_Left,      movewin,         {.ui = WIN_LEFT} },     // 向左移动窗口
{ Mod4Mask,                     XK_Right,     movewin,         {.ui = WIN_RIGHT} },    // 向右移动窗口
{ Mod4Mask,                     XK_k,         movewin,         {.ui = WIN_UP} },       // 向上移动窗口
{ Mod4Mask,                     XK_j,         movewin,         {.ui = WIN_DOWN} },     // 向下移动窗口
{ Mod4Mask,                     XK_h,         movewin,         {.ui = WIN_LEFT} },     // 向左移动窗口
{ Mod4Mask,                     XK_l,         movewin,         {.ui = WIN_RIGHT} },    // 向右移动窗口
{ Mod4Mask|ShiftMask,           XK_k,         resizewin,       {.ui = V_REDUCE} }, // 垂直减少窗口大小
{ Mod4Mask|ShiftMask,           XK_j,         resizewin,       {.ui = V_EXPAND} }, // 垂直增加窗口大小
{ Mod4Mask|ShiftMask,           XK_h,         resizewin,       {.ui = H_REDUCE} }, // 水平减少窗口大小
{ Mod4Mask|ShiftMask,           XK_l,         resizewin,       {.ui = H_EXPAND} }, // 水平增加窗口大小
{ Mod4Mask|ShiftMask,           XK_Up,        resizewin,       {.ui = V_REDUCE} }, // 垂直减少窗口大小
{ Mod4Mask|ShiftMask,           XK_Down,      resizewin,       {.ui = V_EXPAND} }, // 垂直增加窗口大小
{ Mod4Mask|ShiftMask,           XK_Left,      resizewin,       {.ui = H_REDUCE} }, // 水平减少窗口大小
{ Mod4Mask|ShiftMask,           XK_Right,     resizewin,       {.ui = H_EXPAND} }, // 水平增加窗口大小

/* 鼠标控制 */
{ MODKEY|Mod4Mask,              XK_1,         spawn,           {.v = mouseclick1} },  // 鼠标左键点击
{ MODKEY|Mod4Mask,              XK_2,         spawn,           {.v = mouseclick2} },  // 鼠标中键点击
{ MODKEY|Mod4Mask,              XK_3,         spawn,           {.v = mouseclick3} },  // 鼠标右键点击
{ MODKEY|Mod4Mask,              XK_f,         mousefocus,      {0} },                 // 鼠标聚焦到当前选中窗口
{ MODKEY|Mod4Mask,              XK_k,         mousemove,       {.ui = MOUSE_UP} },    // 向上移动鼠标光标
{ MODKEY|Mod4Mask,              XK_l,         mousemove,       {.ui = MOUSE_RIGHT} }, // 向右移动鼠标光标
{ MODKEY|Mod4Mask,              XK_j,         mousemove,       {.ui = MOUSE_DOWM} },  // 向下移动鼠标光标
{ MODKEY|Mod4Mask,              XK_h,         mousemove,       {.ui = MOUSE_LEFT} },  // 向左移动鼠标光标
{ MODKEY|Mod4Mask,              XK_Up,        mousemove,       {.ui = MOUSE_UP} },    // 向上移动鼠标光标
{ MODKEY|Mod4Mask,              XK_Right,     mousemove,       {.ui = MOUSE_RIGHT} }, // 向右移动鼠标光标
{ MODKEY|Mod4Mask,              XK_Down,      mousemove,       {.ui = MOUSE_DOWM} },  // 向下移动鼠标光标
{ MODKEY|Mod4Mask,              XK_Left,      mousemove,       {.ui = MOUSE_LEFT} },  // 向左移动鼠标光标
{ MODKEY|Mod4Mask|ShiftMask,    XK_k,         mousemove,       {.ui = MOUSE_UP + 4*mousemovequick} },    // 向上移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_l,         mousemove,       {.ui = MOUSE_RIGHT + 4*mousemovequick} }, // 向右移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_j,         mousemove,       {.ui = MOUSE_DOWM + 4*mousemovequick} },  // 向下移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_h,         mousemove,       {.ui = MOUSE_LEFT + 4*mousemovequick} },  // 向左移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_Up,        mousemove,       {.ui = MOUSE_UP + 4*mousemovequick} },    // 向上移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_Right,     mousemove,       {.ui = MOUSE_RIGHT + 4*mousemovequick} }, // 向右移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_Down,      mousemove,       {.ui = MOUSE_DOWM + 4*mousemovequick} },  // 向下移动鼠标光标-加速版
{ MODKEY|Mod4Mask|ShiftMask,    XK_Left,      mousemove,       {.ui = MOUSE_LEFT + 4*mousemovequick} },  // 向左移动鼠标光标-加速版
```
Now you can completely disengage from the mouse.

Enjoy it ~
