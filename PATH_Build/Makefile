# 定义编译器和编译选项
CC = aarch64-v01c01-linux-gnu-gcc
CFLAGS = -Wall -g

# 定义头文件搜索路径
INCLUDES = -I../third_lib/hi3519dv500_011/extdrv -I../third_lib/hi3519dv500_011/include

# 定义库文件搜索路径
LDFLAGS = -L../third_lib/hi3519dv500_011/lib

# 定义要链接的库
#LIBS = -lyour_library_name  # 替换为你实际要链接的库名，例如 -laac_comm

# 定义源文件和目标文件
SRCS = Demo_Sample.c  # 替换为你的实际源文件名
OBJS = $(SRCS:.c=.o)

# 定义最终的可执行文件名称
TARGET = Demo_Sample

# 默认目标
all: $(TARGET)

# 链接目标文件生成可执行文件
$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) $(OBJS) $(LDFLAGS) $(LIBS) -o $(TARGET)

# 编译源文件生成目标文件
%.o: %.c
	$(CC) $(CFLAGS) $(INCLUDES) -c $< -o $@

# 清理规则
clean:
	rm -f $(OBJS) $(TARGET)
