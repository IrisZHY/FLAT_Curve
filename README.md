2017.04.26

# Flat
flat disturb

ViewUV::OnLButtonDown
左击点 vector *p
draw_4_principal_Line_UV(pDoc, &dc, p, NULL, NULL, NULL);
g_PD_Line = pDoc->p_group_auto1;
g_PD_Line_count = pDoc->count_group_auto1-1;
 
ViewUV::OnPaint()
//g_PD_Line做控制点 画curve
//BSplint(m_curve)均匀取样的101个点对应的Vector2d坐标p_bSpline_PD_average_2d[i]
	//BSplint(m_curve)均匀取样的101个点对应的Vector3d坐标p_bSpline_PD_average_3d[i]
	//BSplint(m_curve)均匀取样的101个点对应的CPoint坐标pDoc->p_bSpline_PD_average_CPoint[i]
pDoc->p_method_point_group_PD = g_PD_Line;

Flat:
优化点:
g_p_flat_bSpline_2d_PD = g_PD_Line  
( g_PD_Line = pDoc->p_group_auto1)
优化点个数:
g_count_flat_bSpline_2d_PD = g_PD_Line_count - 1  
(g_PD_Line_count = pDoc->count_group_auto1-1)
