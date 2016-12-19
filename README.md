#include <stdio.h>
#include<string.h>

void newCmd() {
	printf("New Cmd function is called!!\n");
}
void openCmd() {
	printf("Open Cmd function is called!!\n");
}
void closeCmd() {
	printf("Close Cmd function is called!!\n");
}
void closeAllCmd() {
	printf("Close All Cmd function is called!!\n");
}
void saveCmd() {
	printf("Save Cmd function is called!!!\n");
}
void saveAsCmd() {
	printf("Save As Cmd function is called!!\n");
}
void saveAllCmd() {
	printf("Save All Cmd function is called!!\n");
}
void printCmd() {
	printf("Print Cmd function is called!!\n");
}
void exitCmd() {
	printf("Exit Cmd function is called!!\n");
}

struct fileCmd {

	char *cmdName;

	void(*cmdPointer)(void);

} file_cmd[] ={ { "new", newCmd },{ "open", openCmd },{ "close", closeCmd },{ "close all", closeAllCmd },{ "save", saveCmd },{ "save as", saveAsCmd },{ "save all", saveAllCmd },{ "print", printCmd },{ "exit", exitCmd } };

int main()
{
	char input[20];
	while (gets(input)!=NULL)
	{
		if (strcmp(input, file_cmd[0].cmdName) == 0) { file_cmd[0].cmdPointer();}
		else if (strcmp(input, file_cmd[1].cmdName) == 0) { file_cmd[1].cmdPointer(); }
		else if (strcmp(input, file_cmd[2].cmdName) == 0) { file_cmd[2].cmdPointer(); }
		else if (strcmp(input, file_cmd[3].cmdName) == 0) { file_cmd[3].cmdPointer(); }
		else if (strcmp(input, file_cmd[4].cmdName) == 0) { file_cmd[4].cmdPointer(); }
		else if (strcmp(input, file_cmd[5].cmdName) == 0) { file_cmd[5].cmdPointer(); }
		else if (strcmp(input, file_cmd[6].cmdName) == 0) { file_cmd[6].cmdPointer(); }
		else if (strcmp(input, file_cmd[7].cmdName) == 0) { file_cmd[7].cmdPointer(); }
		else if (strcmp(input, file_cmd[8].cmdName) == 0) { file_cmd[8].cmdPointer(); exit(1); }
		else { printf("Error\n"); }
	}
    return 0;
}

