# Java_swing

package com.swinglearning;

import java.awt.Color;
import java.awt.Image;
import java.awt.Toolkit;

import javax.swing.*;

public class SimpleFrameTest {
	public static void main(String[] args) {
		SimpleFrame frame=new SimpleFrame();
		Toolkit tool=frame.getToolkit();
		Image myimage=tool.getImage("F:\\eclipse-workspace\\TestFiles\\bin\\com\\swinglearning\\Sleep.gif");
		frame.setBackground(Color.BLUE);
		frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
		frame.setVisible(true);
		frame.setResizable(false);
		frame.setTitle("Test");
		frame.setIconImage(myimage);
	}
}

class SimpleFrame extends JFrame{
	private static final int DEFUALT_WIDTH = 300;
	private static final int DEFUALT_HEIGHT = 200;

	public SimpleFrame() {
		setSize(DEFUALT_WIDTH,DEFUALT_HEIGHT);
	}
}
